
# CalendarObject

The CalendarObject represents a single VEVENT or VTODO within a Calendar.



* Full name: `\Sabre\CalDAV\CalendarObject`
* Parent class: [`\Sabre\DAV\File`](../DAV/File.md)
* This class implements:
[`\Sabre\CalDAV\ICalendarObject`](./ICalendarObject.md), [`\Sabre\DAVACL\IACL`](../DAVACL/IACL.md)



## Properties


### caldavBackend

Sabre\CalDAV\Backend\BackendInterface.

```php
protected \Sabre\CalDAV\Backend\AbstractBackend $caldavBackend
```






***

### objectData

Array with information about this CalendarObject.

```php
protected array $objectData
```






***

### calendarInfo

Array with information about the containing calendar.

```php
protected array $calendarInfo
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CalDAV\Backend\BackendInterface $caldavBackend, array $calendarInfo, array $objectData): mixed
```

The following properties may be passed within $objectData:

* calendarid - This must refer to a calendarid from a caldavBackend
* uri - A unique uri. Only the 'basename' must be passed.
* calendardata (optional) - The iCalendar data
* etag - (optional) The etag for this object, MUST be encloded with
         double-quotes.
* size - (optional) The size of the data in bytes.
* lastmodified - (optional) format as a unix timestamp.
* acl - (optional) Use this to override the default ACL for the node.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caldavBackend` | **\Sabre\CalDAV\Backend\BackendInterface** |  |
| `$calendarInfo` | **array** |  |
| `$objectData` | **array** |  |





***

### getName

Returns the uri for this object.

```php
public getName(): string
```












***

### get

Returns the ICalendar-formatted object.

```php
public get(): string
```












***

### put

Updates the ICalendar-formatted object.

```php
public put(string|resource $calendarData): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarData` | **string&#124;resource** |  |





***

### delete

Deletes the calendar object.

```php
public delete(): mixed
```












***

### getContentType

Returns the mime content-type.

```php
public getContentType(): string
```












***

### getETag

Returns an ETag for this object.

```php
public getETag(): string
```

The ETag is an arbitrary string, but MUST be surrounded by double-quotes.










***

### getLastModified

Returns the last modification date as a unix timestamp.

```php
public getLastModified(): int
```












***

### getSize

Returns the size of this object in bytes.

```php
public getSize(): int
```












***

### getOwner

Returns the owner principal.

```php
public getOwner(): string|null
```

This must be a url to a principal, or null if there's no owner










***

### getACL

Returns a list of ACE's for this node.

```php
public getACL(): array
```

Each ACE has the following properties:
* 'privilege', a string such as {DAV:}read or {DAV:}write. These are
  currently the only supported privileges
* 'principal', a url to the principal who owns the node
* 'protected' (optional), indicating that this ACE is not allowed to
   be updated.










***


## Inherited methods


### getLastModified

Returns the last modification time as a unix timestamp.

```php
public getLastModified(): int
```

If the information is not available, return null.










***

### delete

Deletes the current node.

```php
public delete(): mixed
```











**Throws:**

- [`Forbidden`](../DAV/Exception/Forbidden.md)



***

### setName

Renames the node.

```php
public setName(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | The new name |




**Throws:**

- [`Forbidden`](../DAV/Exception/Forbidden.md)



***

### put

Replaces the contents of the file.

```php
public put(string|resource $data): string|null
```

The data argument is a readable stream resource.

After a successful put operation, you may choose to return an ETag. The
etag must always be surrounded by double-quotes. These quotes must
appear in the actual string you're returning.

Clients may use the ETag from a PUT request to later on make sure that
when they update the file, the contents haven't changed in the mean
time.

If you don't plan to store the file byte-by-byte, and you return a
different object on a subsequent GET you are strongly recommended to not
return an ETag, and just return null.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string&#124;resource** |  |





***

### get

Returns the data.

```php
public get(): mixed
```

This method may either return a string or a readable stream resource










***

### getSize

Returns the size of the file, in bytes.

```php
public getSize(): int
```












***

### getETag

Returns the ETag for a file.

```php
public getETag(): string|null
```

An ETag is a unique identifier representing the current version of the file. If the file changes, the ETag MUST change.
The ETag is an arbitrary string, but MUST be surrounded by double-quotes.

Return null if the ETag can not effectively be determined










***

### getContentType

Returns the mime-type for a file.

```php
public getContentType(): string|null
```

If null is returned, we'll assume application/octet-stream










***

### getOwner

Returns the owner principal.

```php
public getOwner(): string|null
```

This must be a url to a principal, or null if there's no owner










***

### getGroup

Returns a group principal.

```php
public getGroup(): string|null
```

This must be a url to a principal, or null if there's no owner










***

### getACL

Returns a list of ACE's for this node.

```php
public getACL(): array
```

Each ACE has the following properties:
* 'privilege', a string such as {DAV:}read or {DAV:}write. These are
  currently the only supported privileges
* 'principal', a url to the principal who owns the node
* 'protected' (optional), indicating that this ACE is not allowed to
   be updated.










***

### setACL

Updates the ACL.

```php
public setACL(array $acl): mixed
```

This method will receive a list of new ACE's as an array argument.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$acl` | **array** |  |





***

### getSupportedPrivilegeSet

Returns the list of supported privileges for this node.

```php
public getSupportedPrivilegeSet(): array|null
```

The returned data structure is a list of nested privileges.
See Sabre\DAVACL\Plugin::getDefaultSupportedPrivilegeSet for a simple
standard structure.

If null is returned from this method, the default privilege set is used,
which is fine for most common usecases.










***


***
> Automatically generated on 2025-03-15
