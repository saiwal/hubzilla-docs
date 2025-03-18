
# ICSExportPlugin

ICS Exporter.

This plugin adds the ability to export entire calendars as .ics files.
This is useful for clients that don't support CalDAV yet. They often do
support ics files.

To use this, point a http client to a caldav calendar, and add ?expand to
the url.

Further options that can be added to the url:
  start=123456789 - Only return events after the given unix timestamp
  end=123245679   - Only return events from before the given unix timestamp
  expand=1        - Strip timezone information and expand recurring events.
                    If you'd like to expand, you _must_ also specify start
                    and end.

By default this plugin returns data in the text/calendar format (iCalendar
2.0). If you'd like to receive jCal data instead, you can use an Accept
header:

Accept: application/calendar+json

Alternatively, you can also specify this in the url using
accept=application/calendar+json, or accept=jcal for short. If the url
parameter and Accept header is specified, the url parameter wins.

Note that specifying a start or end data implies that only events will be
returned. VTODO and VJOURNAL will be stripped.

* Full name: `\Sabre\CalDAV\ICSExportPlugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../DAV/ServerPlugin.md)



## Properties


### server

Reference to Server class.

```php
protected \Sabre\DAV\Server $server
```






***

## Methods


### initialize

Initializes the plugin and registers event handlers.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### httpGet

Intercepts GET requests on calendar urls ending with ?export.

```php
public httpGet(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |




**Throws:**

- [`BadRequest`](../DAV/Exception/BadRequest.md)

- [`NotFound`](../DAV/Exception/NotFound.md)

- [`InvalidDataException`](../VObject/InvalidDataException.md)



***

### generateResponse

This method is responsible for generating the actual, full response.

```php
protected generateResponse(string $path, \DateTime|null $start, \DateTime|null $end, bool $expand, string $componentType, string $format, array $properties, \Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$start` | **\DateTime&#124;null** |  |
| `$end` | **\DateTime&#124;null** |  |
| `$expand` | **bool** |  |
| `$componentType` | **string** |  |
| `$format` | **string** |  |
| `$properties` | **array** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |




**Throws:**

- [`NotFound`](../DAV/Exception/NotFound.md)

- [`InvalidDataException`](../VObject/InvalidDataException.md)



***

### mergeObjects

Merges all calendar objects, and builds one big iCalendar blob.

```php
public mergeObjects(array $properties, array $inputObjects): \Sabre\VObject\Component\VCalendar
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **array** | Some CalDAV properties |
| `$inputObjects` | **array** |  |





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
> Automatically generated on 2025-03-18
