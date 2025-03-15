***

# Plugin

PropertyStorage Plugin.

Adding this plugin to your server allows clients to store any arbitrary
WebDAV property.

See:
  http://sabre.io/dav/property-storage/

for more information.

* Full name: `\Sabre\DAV\PropertyStorage\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../ServerPlugin.md)



## Properties


### pathFilter

If you only want this plugin to store properties for a limited set of
paths, you can use a pathFilter to do this.

```php
public callable $pathFilter
```

The pathFilter should be a callable. The callable retrieves a path as
its argument, and should return true or false whether it allows
properties to be stored.




***

### backend



```php
public \Sabre\DAV\PropertyStorage\Backend\BackendInterface $backend
```






***

## Methods


### __construct

Creates the plugin.

```php
public __construct(\Sabre\DAV\PropertyStorage\Backend\BackendInterface $backend): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$backend` | **\Sabre\DAV\PropertyStorage\Backend\BackendInterface** |  |





***

### initialize

This initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This function is called by Sabre\DAV\Server, after
addPlugin is called.

This method should set up the required event subscriptions.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### propFind

Called during PROPFIND operations.

```php
public propFind(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

If there's any requested properties that don't have a value yet, this
plugin will look in the property storage backend to find them.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### propPatch

Called during PROPPATCH operations.

```php
public propPatch(string $path, \Sabre\DAV\PropPatch $propPatch): mixed
```

If there's any updated properties that haven't been stored, the
propertystorage backend can handle it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### afterUnbind

Called after a node is deleted.

```php
public afterUnbind(string $path): mixed
```

This allows the backend to clean up any properties still in the
database.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### afterMove

Called after a node is moved.

```php
public afterMove(string $source, string $destination): mixed
```

This allows the backend to move all the associated properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |
| `$destination` | **string** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
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
