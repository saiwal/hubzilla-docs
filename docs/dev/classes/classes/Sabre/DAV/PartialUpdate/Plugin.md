***

# Plugin

Partial update plugin (Patch method).

This plugin provides a way to modify only part of a target resource
It may bu used to update a file chunk, upload big a file into smaller
chunks or resume an upload.

$patchPlugin = new \Sabre\DAV\PartialUpdate\Plugin();
$server->addPlugin($patchPlugin);

* Full name: `\Sabre\DAV\PartialUpdate\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../ServerPlugin.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`RANGE_APPEND`|public| |1|
|`RANGE_START`|public| |2|
|`RANGE_END`|public| |3|

## Properties


### server

Reference to server.

```php
protected \Sabre\DAV\Server $server
```






***

## Methods


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
using DAV\Server::getPlugin










***

### getHTTPMethods

Use this method to tell the server this plugin defines additional
HTTP methods.

```php
public getHTTPMethods(string $uri): array
```

This method is passed a uri. It should only return HTTP methods that are
available for the specified uri.

We claim to support PATCH method (partirl update) if and only if
    - the node exist
    - the node implements our partial update interface






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












***

### httpPatch

Patch an uri.

```php
public httpPatch(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

The WebDAV patch request can be used to modify only a part of an
existing resource. If the resource does not exist yet and the first
offset is not 0, the request fails






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### getHTTPUpdateRange

Returns the HTTP custom range update header.

```php
public getHTTPUpdateRange(\Sabre\HTTP\RequestInterface $request): array|null
```

This method returns null if there is no well-formed HTTP range request
header. It returns array(1) if it was an append request, array(2,
$start, $end) if it's a start and end range, lastly it's array(3,
$endoffset) if the offset was negative, and should be calculated from
the end of the file.

Examples:

null - invalid
[1] - append
[2,10,15] - update bytes 10, 11, 12, 13, 14, 15
[2,10,null] - update bytes 10 until the end of the patch body
[3,-5] - update from 5 bytes from the end of the file.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |





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
