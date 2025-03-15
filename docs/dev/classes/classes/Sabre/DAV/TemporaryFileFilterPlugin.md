***

# TemporaryFileFilterPlugin

Temporary File Filter Plugin.

The purpose of this filter is to intercept some of the garbage files
operation systems and applications tend to generate when mounting
a WebDAV share as a disk.

It will intercept these files and place them in a separate directory.
these files are not deleted automatically, so it is advisable to
delete these after they are not accessed for 24 hours.

Currently it supports:
  * OS/X style resource forks and .DS_Store
  * desktop.ini and Thumbs.db (windows)
  * .*.swp (vim temporary files)
  * .dat.* (smultron temporary files)

Additional patterns can be added, by adding on to the
temporaryFilePatterns property.

* Full name: `\Sabre\DAV\TemporaryFileFilterPlugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](./ServerPlugin.md)



## Properties


### temporaryFilePatterns

This is the list of patterns we intercept.

```php
public array $temporaryFilePatterns
```

If new patterns are added, they must be valid patterns for preg_match.




***

### server

A reference to the main Server class.

```php
protected \Sabre\DAV\Server $server
```






***

### dataDir

This is the directory where this plugin
will store it's files.

```php
private string $dataDir
```






***

## Methods


### __construct

Creates the plugin.

```php
public __construct(string|null $dataDir = null): mixed
```

Make sure you specify a directory for your files. If you don't, we
will use PHP's directory for session-storage instead, and you might
not want that.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dataDir` | **string&#124;null** |  |





***

### initialize

Initialize the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This is called automatically be the Server class after this plugin is
added with Sabre\DAV\Server::addPlugin()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### beforeMethod

This method is called before any HTTP method handler.

```php
public beforeMethod(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

This method intercepts any GET, DELETE, PUT and PROPFIND calls to
filenames that are known to match the 'temporary file' regex.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### beforeCreateFile

This method is invoked if some subsystem creates a new file.

```php
public beforeCreateFile(string $uri, resource $data, \Sabre\DAV\ICollection $parent, bool $modified): bool
```

This is used to deal with HTTP LOCK requests which create a new
file.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$data` | **resource** |  |
| `$parent` | **\Sabre\DAV\ICollection** |  |
| `$modified` | **bool** | should be set to true, if this event handler<br />changed &amp;$data |





***

### isTempFile

This method will check if the url matches the temporary file pattern
if it does, it will return an path based on $this->dataDir for the
temporary file storage.

```php
protected isTempFile(string $path): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### httpGet

This method handles the GET method for temporary files.

```php
public httpGet(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $hR, string $tempLocation): bool
```

If the file doesn't exist, it will return false which will kick in
the regular system for the GET method.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$hR` | **\Sabre\HTTP\ResponseInterface** |  |
| `$tempLocation` | **string** |  |





***

### httpPut

This method handles the PUT method.

```php
public httpPut(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $hR, string $tempLocation): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$hR` | **\Sabre\HTTP\ResponseInterface** |  |
| `$tempLocation` | **string** |  |





***

### httpDelete

This method handles the DELETE method.

```php
public httpDelete(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $hR, string $tempLocation): bool
```

If the file didn't exist, it will return false, which will make the
standard HTTP DELETE handler kick in.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$hR` | **\Sabre\HTTP\ResponseInterface** |  |
| `$tempLocation` | **string** |  |





***

### httpPropfind

This method handles the PROPFIND method.

```php
public httpPropfind(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $hR, string $tempLocation): bool
```

It's a very lazy method, it won't bother checking the request body
for which properties were requested, and just sends back a default
set of properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$hR` | **\Sabre\HTTP\ResponseInterface** |  |
| `$tempLocation` | **string** |  |





***

### getDataDir

This method returns the directory where the temporary files should be stored.

```php
protected getDataDir(): string
```












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
