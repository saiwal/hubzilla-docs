***

# Plugin

Browser Plugin.

This plugin provides a html representation, so that a WebDAV server may be accessed
using a browser.

The class intercepts GET requests to collection resources and generates a simple
html index.

* Full name: `\Sabre\DAV\Browser\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../ServerPlugin.md)



## Properties


### server

reference to server class.

```php
protected \Sabre\DAV\Server $server
```






***

### enablePost

enablePost turns on the 'actions' panel, which allows people to create
folders and upload files straight from a browser.

```php
protected bool $enablePost
```






***

### uninterestingProperties

A list of properties that are usually not interesting. This can cut down
the browser output a bit by removing the properties that most people
will likely not want to see.

```php
public array $uninterestingProperties
```






***

## Methods


### __construct

Creates the object.

```php
public __construct(bool $enablePost = true): mixed
```

By default it will allow file creation and uploads.
Specify the first argument as false to disable this






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enablePost` | **bool** |  |





***

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

### httpGetEarly

This method intercepts GET requests that have ?sabreAction=info
appended to the URL.

```php
public httpGetEarly(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpGet

This method intercepts GET requests to collections and returns the html.

```php
public httpGet(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### httpPOST

Handles POST requests for tree operations.

```php
public httpPOST(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### escapeHTML

Escapes a string for html.

```php
public escapeHTML(string $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





***

### generateDirectoryIndex

Generates the html directory index for a given url.

```php
public generateDirectoryIndex(string $path): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### generatePluginListing

Generates the 'plugins' page.

```php
public generatePluginListing(): string
```












***

### generateHeader

Generates the first block of HTML, including the <head> tag and page
header.

```php
public generateHeader(string $title, string $path = null): string
```

Returns footer.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$title` | **string** |  |
| `$path` | **string** |  |





***

### generateFooter

Generates the page footer.

```php
public generateFooter(): string
```

Returns html.










***

### htmlActionsPanel

This method is used to generate the 'actions panel' output for
collections.

```php
public htmlActionsPanel(\Sabre\DAV\INode $node, mixed& $output, string $path): mixed
```

This specifically generates the interfaces for creating new files, and
creating new directories.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Sabre\DAV\INode** |  |
| `$output` | **mixed** |  |
| `$path` | **string** |  |





***

### getAssetUrl

This method takes a path/name of an asset and turns it into url
suiteable for http access.

```php
protected getAssetUrl(string $assetName): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$assetName` | **string** |  |





***

### getLocalAssetPath

This method returns a local pathname to an asset.

```php
protected getLocalAssetPath(string $assetName): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$assetName` | **string** |  |




**Throws:**

- [`NotFound`](../Exception/NotFound.md)



***

### serveAsset

This method reads an asset from disk and generates a full http response.

```php
protected serveAsset(string $assetName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$assetName` | **string** |  |





***

### compareNodes

Sort helper function: compares two directory entries based on type and
display name. Collections sort above other types.

```php
protected compareNodes(array $a, array $b): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **array** |  |
| `$b` | **array** |  |





***

### mapResourceType

Maps a resource type to a human-readable string and icon.

```php
private mapResourceType(array $resourceTypes, \Sabre\DAV\INode $node): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$resourceTypes` | **array** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### drawPropertyRow

Draws a table row for a property.

```php
private drawPropertyRow(string $name, mixed $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### drawPropertyValue

Draws a table row for a property.

```php
private drawPropertyValue(\Sabre\DAV\Browser\HtmlOutputHelper $html, mixed $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **\Sabre\DAV\Browser\HtmlOutputHelper** |  |
| `$value` | **mixed** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins;
using \Sabre\DAV\Server::getPlugin










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
