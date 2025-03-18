
# Plugin

CardDAV plugin.

The CardDAV plugin adds CardDAV functionality to the WebDAV server

* Full name: `\Sabre\CardDAV\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../DAV/ServerPlugin.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`ADDRESSBOOK_ROOT`|public| |&#039;addressbooks&#039;|
|`NS_CARDDAV`|public| |&#039;urn:ietf:params:xml:ns:carddav&#039;|

## Properties


### directories

Add urls to this property to have them automatically exposed as
'directories' to the user.

```php
public array $directories
```






***

### server

Server class.

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

### getFeatures

Returns a list of supported features.

```php
public getFeatures(): array
```

This is used in the DAV: header in the OPTIONS and PROPFIND requests.










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

### propFindEarly

Adds all CardDAV-specific properties.

```php
public propFindEarly(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### report

This functions handles REPORT requests specific to CardDAV.

```php
public report(string $reportName, \DOMNode $dom, mixed $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reportName` | **string** |  |
| `$dom` | **\DOMNode** |  |
| `$path` | **mixed** |  |





***

### getAddressbookHomeForPrincipal

Returns the addressbook home for a given principal.

```php
protected getAddressbookHomeForPrincipal(string $principal): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principal` | **string** |  |





***

### addressbookMultiGetReport

This function handles the addressbook-multiget REPORT.

```php
public addressbookMultiGetReport(\Sabre\CardDAV\Xml\Request\AddressBookMultiGetReport $report): mixed
```

This report is used by the client to fetch the content of a series
of urls. Effectively avoiding a lot of redundant requests.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$report` | **\Sabre\CardDAV\Xml\Request\AddressBookMultiGetReport** |  |





***

### beforeWriteContent

This method is triggered before a file gets updated with new content.

```php
public beforeWriteContent(string $path, \Sabre\DAV\IFile $node, resource& $data, bool& $modified): mixed
```

This plugin uses this method to ensure that Card nodes receive valid
vcard data.






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

This plugin uses this method to ensure that Card nodes receive valid
vcard data.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$data` | **resource** |  |
| `$parentNode` | **\Sabre\DAV\ICollection** |  |
| `$modified` | **bool** | should be set to true, if this event handler<br />changed &amp;$data |





***

### validateVCard

Checks if the submitted iCalendar data is in fact, valid.

```php
protected validateVCard(resource|string& $data, bool& $modified): mixed
```

An exception is thrown if it's not.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource&#124;string** |  |
| `$modified` | **bool** | should be set to true, if this event handler<br />changed &amp;$data |





***

### addressbookQueryReport

This function handles the addressbook-query REPORT.

```php
protected addressbookQueryReport(\Sabre\CardDAV\Xml\Request\AddressBookQueryReport $report): mixed
```

This report is used by the client to filter an addressbook based on a
complex query.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$report` | **\Sabre\CardDAV\Xml\Request\AddressBookQueryReport** |  |





***

### validateFilters

Validates if a vcard makes it throught a list of filters.

```php
public validateFilters(string $vcardData, array $filters, string $test): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vcardData` | **string** |  |
| `$filters` | **array** |  |
| `$test` | **string** | anyof or allof (which means OR or AND) |





***

### validateParamFilters

Validates if a param-filter can be applied to a specific property.

```php
protected validateParamFilters(array $vProperties, array $filters, string $test): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vProperties` | **array** |  |
| `$filters` | **array** |  |
| `$test` | **string** |  |





***

### validateTextMatches

Validates if a text-filter can be applied to a specific property.

```php
protected validateTextMatches(array $texts, array $filters, string $test): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$texts` | **array** |  |
| `$filters` | **array** |  |
| `$test` | **string** |  |





***

### propFindLate

This event is triggered when fetching properties.

```php
public propFindLate(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

This event is scheduled late in the process, after most work for
propfind has been done.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### htmlActionsPanel

This method is used to generate HTML output for the
Sabre\DAV\Browser\Plugin. This allows us to generate an interface users
can use to create new addressbooks.

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

### negotiateVCard

This helper function performs the content-type negotiation for vcards.

```php
protected negotiateVCard(string $input, string& $mimeType = null): string
```

It will return one of the following strings:
1. vcard3
2. vcard4
3. jcard

It defaults to vcard3.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** |  |
| `$mimeType` | **string** |  |





***

### convertVCard

Converts a vcard blob to a different version, or jcard.

```php
protected convertVCard(string|resource $data, string $target, array $propertiesFilter = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string&#124;resource** |  |
| `$target` | **string** |  |
| `$propertiesFilter` | **array** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using DAV\Server::getPlugin










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
