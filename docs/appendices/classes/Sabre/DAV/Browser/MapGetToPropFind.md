
# MapGetToPropFind

This is a simple plugin that will map any GET request for non-files to
PROPFIND allprops-requests.

This should allow easy debugging of PROPFIND

* Full name: `\Sabre\DAV\Browser\MapGetToPropFind`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../ServerPlugin.md)



## Properties


### server

reference to server class.

```php
protected \Sabre\DAV\Server $server
```






***

## Methods


### initialize

Initializes the plugin and subscribes to events.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### httpGet

This method intercepts GET requests to non-files, and changes it into an HTTP PROPFIND request.

```php
public httpGet(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





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
