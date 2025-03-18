
# Plugin

This plugin all WebDAV-sync capabilities to the Server.

WebDAV-sync is defined by rfc6578

The sync capabilities only work with collections that implement
Sabre\DAV\Sync\ISyncCollection.

* Full name: `\Sabre\DAV\Sync\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../ServerPlugin.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`SYNCTOKEN_PREFIX`|public| |&#039;http://sabre.io/ns/sync/&#039;|

## Properties


### server

Reference to server object.

```php
protected \Sabre\DAV\Server $server
```






***

## Methods


### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using \Sabre\DAV\Server::getPlugin










***

### initialize

Initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This is when the plugin registers it's hooks.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





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

### syncCollection

This method handles the {DAV:}sync-collection HTTP REPORT.

```php
public syncCollection(string $uri, \Sabre\DAV\Xml\Request\SyncCollectionReport $report): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$report` | **\Sabre\DAV\Xml\Request\SyncCollectionReport** |  |





***

### sendSyncCollectionResponse

Sends the response to a sync-collection request.

```php
protected sendSyncCollectionResponse(string $syncToken, string $collectionUrl, array $added, array $modified, array $deleted, array $properties, bool $resultTruncated = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$syncToken` | **string** |  |
| `$collectionUrl` | **string** |  |
| `$added` | **array** |  |
| `$modified` | **array** |  |
| `$deleted` | **array** |  |
| `$properties` | **array** |  |
| `$resultTruncated` | **bool** |  |





***

### propFind

This method is triggered whenever properties are requested for a node.

```php
public propFind(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

We intercept this to see if we must return a {DAV:}sync-token.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### validateTokens

The validateTokens event is triggered before every request.

```php
public validateTokens(\Sabre\HTTP\RequestInterface $request, array& $conditions): mixed
```

It's a moment where this plugin can check all the supplied lock tokens
in the If: header, and check if they are valid.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$conditions` | **array** |  |





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
