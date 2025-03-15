
# Plugin

CalDAV plugin.

This plugin provides functionality added by CalDAV (RFC 4791)
It implements new reports, and the MKCALENDAR method.

* Full name: `\Sabre\CalDAV\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../DAV/ServerPlugin.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`NS_CALDAV`|public| |&#039;urn:ietf:params:xml:ns:caldav&#039;|
|`NS_CALENDARSERVER`|public| |&#039;http://calendarserver.org/ns/&#039;|
|`CALENDAR_ROOT`|public| |&#039;calendars&#039;|

## Properties


### server

Reference to server object.

```php
protected \Sabre\DAV\Server $server
```






***

### maxResourceSize

The default PDO storage uses a MySQL MEDIUMBLOB for iCalendar data,
which can hold up to 2^24 = 16777216 bytes. This is plenty. We're
capping it to 10M here.

```php
protected $maxResourceSize
```






***

## Methods


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

### getCalendarHomeForPrincipal

Returns the path to a principal's calendar home.

```php
public getCalendarHomeForPrincipal(string $principalUrl): string
```

The return url must not end with a slash.
This function should return null in case a principal did not have
a calendar home.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalUrl` | **string** |  |





***

### getFeatures

Returns a list of features for the DAV: HTTP header.

```php
public getFeatures(): array
```












***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using DAV\Server::getPlugin










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

### initialize

Initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### report

This functions handles REPORT requests specific to CalDAV.

```php
public report(string $reportName, mixed $report, mixed $path): bool|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reportName` | **string** |  |
| `$report` | **mixed** |  |
| `$path` | **mixed** |  |





***

### httpMkCalendar

This function handles the MKCALENDAR HTTP method, which creates
a new calendar.

```php
public httpMkCalendar(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### propFind

PropFind.

```php
public propFind(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

This method handler is invoked before any after properties for a
resource are fetched. This allows us to add in any CalDAV specific
properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### calendarMultiGetReport

This function handles the calendar-multiget REPORT.

```php
public calendarMultiGetReport(\Sabre\CalDAV\Xml\Request\CalendarMultiGetReport $report): mixed
```

This report is used by the client to fetch the content of a series
of urls. Effectively avoiding a lot of redundant requests.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$report` | **\Sabre\CalDAV\Xml\Request\CalendarMultiGetReport** |  |





***

### calendarQueryReport

This function handles the calendar-query REPORT.

```php
public calendarQueryReport(\Sabre\CalDAV\Xml\Request\CalendarQueryReport $report): mixed
```

This report is used by clients to request calendar objects based on
complex conditions.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$report` | **\Sabre\CalDAV\Xml\Request\CalendarQueryReport** |  |





***

### freeBusyQueryReport

This method is responsible for parsing the request and generating the
response for the CALDAV:free-busy-query REPORT.

```php
protected freeBusyQueryReport(\Sabre\CalDAV\Xml\Request\FreeBusyQueryReport $report): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$report` | **\Sabre\CalDAV\Xml\Request\FreeBusyQueryReport** |  |





***

### beforeWriteContent

This method is triggered before a file gets updated with new content.

```php
public beforeWriteContent(string $path, \Sabre\DAV\IFile $node, resource& $data, bool& $modified): mixed
```

This plugin uses this method to ensure that CalDAV objects receive
valid calendar data.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$node` | **\Sabre\DAV\IFile** |  |
| `$data` | **resource** |  |
| `$modified` | **bool** | should be set to true, if this event handler<br />changed &amp;$data |





***

### beforeCreateFile

This method is triggered before a new file is created.

```php
public beforeCreateFile(string $path, resource& $data, \Sabre\DAV\ICollection $parentNode, bool& $modified): mixed
```

This plugin uses this method to ensure that newly created calendar
objects contain valid calendar data.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$data` | **resource** |  |
| `$parentNode` | **\Sabre\DAV\ICollection** |  |
| `$modified` | **bool** | should be set to true, if this event handler<br />changed &amp;$data |





***

### validateICalendar

Checks if the submitted iCalendar data is in fact, valid.

```php
protected validateICalendar(resource|string& $data, string $path, bool& $modified, \Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response, bool $isNew): mixed
```

An exception is thrown if it's not.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource&#124;string** |  |
| `$path` | **string** |  |
| `$modified` | **bool** | should be set to true, if this event handler<br />changed &amp;$data |
| `$request` | **\Sabre\HTTP\RequestInterface** | the http request |
| `$response` | **\Sabre\HTTP\ResponseInterface** | the http response |
| `$isNew` | **bool** | is the item a new one, or an update |





***

### getSupportedPrivilegeSet

This method is triggered whenever a subsystem reqeuests the privileges
that are supported on a particular node.

```php
public getSupportedPrivilegeSet(\Sabre\DAV\INode $node, array& $supportedPrivilegeSet): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Sabre\DAV\INode** |  |
| `$supportedPrivilegeSet` | **array** |  |





***

### htmlActionsPanel

This method is used to generate HTML output for the
DAV\Browser\Plugin. This allows us to generate an interface users
can use to create new calendars.

```php
public htmlActionsPanel(\Sabre\DAV\INode $node, string& $output): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Sabre\DAV\INode** |  |
| `$output` | **string** |  |





***

### httpAfterGet

This event is triggered after GET requests.

```php
public httpAfterGet(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

This is used to transform data into jCal, if this was requested.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





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
