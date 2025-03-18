
# Plugin

Locking plugin.

This plugin provides locking support to a WebDAV server.
The easiest way to get started, is by hooking it up as such:

$lockBackend = new Sabre\DAV\Locks\Backend\File('./mylockdb');
$lockPlugin = new Sabre\DAV\Locks\Plugin($lockBackend);
$server->addPlugin($lockPlugin);

* Full name: `\Sabre\DAV\Locks\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../ServerPlugin.md)



## Properties


### locksBackend

locksBackend.

```php
protected \Sabre\DAV\Locks\Backend\BackendInterface $locksBackend
```






***

### server

server.

```php
protected \Sabre\DAV\Server $server
```






***

## Methods


### __construct

__construct.

```php
public __construct(\Sabre\DAV\Locks\Backend\BackendInterface $locksBackend): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locksBackend` | **\Sabre\DAV\Locks\Backend\BackendInterface** |  |





***

### initialize

Initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This method is automatically called by the Server class after addPlugin.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using Sabre\DAV\Server::getPlugin










***

### propFind

This method is called after most properties have been found
it allows us to add in any Lock-related properties.

```php
public propFind(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### getHTTPMethods

Use this method to tell the server this plugin defines additional
HTTP methods.

```php
public getHTTPMethods(string $uri): array
```

This method is passed a uri. It should only return HTTP methods that are
available for the specified uri.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getFeatures

Returns a list of features for the HTTP OPTIONS Dav: header.

```php
public getFeatures(): array
```

In this case this is only the number 2. The 2 in the Dav: header
indicates the server supports locks.










***

### getLocks

Returns all lock information on a particular uri.

```php
public getLocks(string $uri, bool $returnChildLocks = false): array
```

This function should return an array with Sabre\DAV\Locks\LockInfo objects. If there are no locks on a file, return an empty array.

Additionally there is also the possibility of locks on parent nodes, so we'll need to traverse every part of the tree
If the $returnChildLocks argument is set to true, we'll also traverse all the children of the object
for any possible locks and return those as well.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$returnChildLocks` | **bool** |  |





***

### httpLock

Locks an uri.

```php
public httpLock(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

The WebDAV lock request can be operated to either create a new lock on a file, or to refresh an existing lock
If a new lock is created, a full XML body should be supplied, containing information about the lock such as the type
of lock (shared or exclusive) and the owner of the lock

If a lock is to be refreshed, no body should be supplied and there should be a valid If header containing the lock

Additionally, a lock can be requested for a non-existent file. In these case we're obligated to create an empty file as per RFC4918:S7.3






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpUnlock

Unlocks a uri.

```php
public httpUnlock(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

This WebDAV method allows you to remove a lock from a node. The client should provide a valid locktoken through the Lock-token http header
The server should return 204 (No content) on success






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### afterUnbind

This method is called after a node is deleted.

```php
public afterUnbind(string $path): mixed
```

We use this event to clean up any locks that still exist on the node.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### lockNode

Locks a uri.

```php
public lockNode(string $uri, \Sabre\DAV\Locks\LockInfo $lockInfo): bool
```

All the locking information is supplied in the lockInfo object. The object has a suggested timeout, but this can be safely ignored
It is important that if the existing timeout is ignored, the property is overwritten, as this needs to be sent back to the client






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$lockInfo` | **\Sabre\DAV\Locks\LockInfo** |  |





***

### unlockNode

Unlocks a uri.

```php
public unlockNode(string $uri, \Sabre\DAV\Locks\LockInfo $lockInfo): bool
```

This method removes a lock from a uri. It is assumed all the supplied information is correct and verified






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$lockInfo` | **\Sabre\DAV\Locks\LockInfo** |  |





***

### getTimeoutHeader

Returns the contents of the HTTP Timeout header.

```php
public getTimeoutHeader(): int
```

The method formats the header into an integer.










***

### generateLockResponse

Generates the response for successful LOCK requests.

```php
protected generateLockResponse(\Sabre\DAV\Locks\LockInfo $lockInfo): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lockInfo` | **\Sabre\DAV\Locks\LockInfo** |  |





***

### validateTokens

The validateTokens event is triggered before every request.

```php
public validateTokens(\Sabre\HTTP\RequestInterface $request, mixed& $conditions): mixed
```

It's a moment where this plugin can check all the supplied lock tokens
in the If: header, and check if they are valid.

In addition, it will also ensure that it checks any missing lokens that
must be present in the request, and reject requests without the proper
tokens.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$conditions` | **mixed** |  |





***

### parseLockRequest

Parses a webdav lock xml body, and returns a new Sabre\DAV\Locks\LockInfo object.

```php
protected parseLockRequest(string $body): \Sabre\DAV\Locks\LockInfo
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$body` | **string** |  |





***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


## Inherited methods


### initialize

This initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This function is called by Sabre\DAV\Server, after
addPlugin is called.

This method should set up the required event subscriptions.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getFeatures

This method should return a list of server-features.

```php
public getFeatures(): array
```

This is for example 'versioning' and is added to the DAV: header
in an OPTIONS response.










***

### getHTTPMethods

Use this method to tell the server this plugin defines additional
HTTP methods.

```php
public getHTTPMethods(string $path): array
```

This method is passed a uri. It should only return HTTP methods that are
available for the specified uri.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using \Sabre\DAV\Server::getPlugin










***

### getSupportedReportSet

Returns a list of reports this plugin supports.

```php
public getSupportedReportSet(string $uri): array
```

This will be used in the {DAV:}supported-report-set property.
Note that you still need to subscribe to the 'report' event to actually
implement them






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


***
> Automatically generated on 2025-03-18
