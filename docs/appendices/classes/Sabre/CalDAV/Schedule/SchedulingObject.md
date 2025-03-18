
# SchedulingObject

The SchedulingObject represents a scheduling object in the Inbox collection.



* Full name: `\Sabre\CalDAV\Schedule\SchedulingObject`
* Parent class: [`\Sabre\CalDAV\CalendarObject`](../CalendarObject.md)
* This class implements:
[`\Sabre\CalDAV\Schedule\ISchedulingObject`](./ISchedulingObject.md)




## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CalDAV\Backend\SchedulingSupport $caldavBackend, array $objectData): mixed
```

The following properties may be passed within $objectData:

* uri - A unique uri. Only the 'basename' must be passed.
* principaluri - the principal that owns the object.
* calendardata (optional) - The iCalendar data
* etag - (optional) The etag for this object, MUST be encloded with
         double-quotes.
* size - (optional) The size of the data in bytes.
* lastmodified - (optional) format as a unix timestamp.
* acl - (optional) Use this to override the default ACL for the node.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caldavBackend` | **\Sabre\CalDAV\Backend\SchedulingSupport** |  |
| `$objectData` | **array** |  |





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

Deletes the scheduling message.

```php
public delete(): mixed
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

Returns the last modification date as a unix timestamp.

```php
public getLastModified(): int
```












***

### delete

Deletes the calendar object.

```php
public delete(): mixed
```












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

- [`Forbidden`](../../DAV/Exception/Forbidden.md)



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

### get

Returns the ICalendar-formatted object.

```php
public get(): string
```












***

### getSize

Returns the size of this object in bytes.

```php
public getSize(): int
```












***

### getETag

Returns an ETag for this object.

```php
public getETag(): string
```

The ETag is an arbitrary string, but MUST be surrounded by double-quotes.










***

### getContentType

Returns the mime content-type.

```php
public getContentType(): string
```












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


***
> Automatically generated on 2025-03-18
