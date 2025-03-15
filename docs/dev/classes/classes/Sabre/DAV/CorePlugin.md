***

# CorePlugin

The core plugin provides all the basic features for a WebDAV server.



* Full name: `\Sabre\DAV\CorePlugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](./ServerPlugin.md)



## Properties


### server

Reference to server object.

```php
protected \Sabre\DAV\Server $server
```






***

## Methods


### initialize

Sets up the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```








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
using DAV\Server::getPlugin










***

### httpGet

This is the default implementation for the GET method.

```php
public httpGet(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpOptions

HTTP OPTIONS.

```php
public httpOptions(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpHead

HTTP HEAD.

```php
public httpHead(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

This method is normally used to take a peak at a url, and only get the
HTTP response headers, without the body. This is used by clients to
determine if a remote file was changed, so they can use a local cached
version, instead of downloading it again






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpDelete

HTTP Delete.

```php
public httpDelete(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

The HTTP delete method, deletes a given uri






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpPropFind

WebDAV PROPFIND.

```php
public httpPropFind(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

This WebDAV method requests information about an uri resource, or a list of resources
If a client wants to receive the properties for a single resource it will add an HTTP Depth: header with a 0 value
If the value is 1, it means that it also expects a list of sub-resources (e.g.: files in a directory)

The request body contains an XML data structure that has a list of properties the client understands
The response body is also an xml document, containing information about every uri resource and the requested properties

It has to return a HTTP 207 Multi-status status code






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpPropPatch

WebDAV PROPPATCH.

```php
public httpPropPatch(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

This method is called to update properties on a Node. The request is an XML body with all the mutations.
In this XML body it is specified which properties should be set/updated and/or deleted






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpPut

HTTP PUT method.

```php
public httpPut(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

This HTTP method updates a file, or creates a new one.

If a new resource was created, a 201 Created status code should be returned. If an existing resource is updated, it's a 204 No Content






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpMkcol

WebDAV MKCOL.

```php
public httpMkcol(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

The MKCOL method is used to create a new collection (directory) on the server






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpMove

WebDAV HTTP MOVE method.

```php
public httpMove(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

This method moves one uri to a different uri. A lot of the actual request processing is done in getCopyMoveInfo






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpCopy

WebDAV HTTP COPY method.

```php
public httpCopy(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

This method copies one uri to a different uri, and works much like the MOVE request
A lot of the actual request processing is done in getCopyMoveInfo






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpReport

HTTP REPORT method implementation.

```php
public httpReport(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

Although the REPORT method is not part of the standard WebDAV spec (it's from rfc3253)
It's used in a lot of extensions, so it made sense to implement it into the core.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### propPatchProtectedPropertyCheck

This method is called during property updates.

```php
public propPatchProtectedPropertyCheck(string $path, \Sabre\DAV\PropPatch $propPatch): mixed
```

Here we check if a user attempted to update a protected property and
ensure that the process fails if this is the case.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### propPatchNodeUpdate

This method is called during property updates.

```php
public propPatchNodeUpdate(string $path, \Sabre\DAV\PropPatch $propPatch): mixed
```

Here we check if a node implements IProperties and let the node handle
updating of (some) properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### propFind

This method is called when properties are retrieved.

```php
public propFind(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

Here we add all the default properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### propFindNode

Fetches properties for a node.

```php
public propFindNode(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

This event is called a bit later, so plugins have a chance first to
populate the result.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### propFindLate

This method is called when properties are retrieved.

```php
public propFindLate(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

This specific handler is called very late in the process, because we
want other systems to first have a chance to handle the properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### exception

Listens for exception events, and automatically logs them.

```php
public exception(\Sabre\DAV\Exception $e): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$e` | **\Sabre\DAV\Exception** |  |





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
> Automatically generated on 2025-03-15
