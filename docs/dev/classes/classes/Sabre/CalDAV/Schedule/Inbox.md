***

# Inbox

The CalDAV scheduling inbox.



* Full name: `\Sabre\CalDAV\Schedule\Inbox`
* Parent class: [`\Sabre\DAV\Collection`](../../DAV/Collection.md)
* This class implements:
[`\Sabre\CalDAV\Schedule\IInbox`](./IInbox.md)



## Properties


### caldavBackend

CalDAV backend.

```php
protected \Sabre\CalDAV\Backend\BackendInterface $caldavBackend
```






***

### principalUri

The principal Uri.

```php
protected string $principalUri
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CalDAV\Backend\SchedulingSupport $caldavBackend, string $principalUri): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caldavBackend` | **\Sabre\CalDAV\Backend\SchedulingSupport** |  |
| `$principalUri` | **string** |  |





***

### getName

Returns the name of the node.

```php
public getName(): string
```

This is used to generate the url.










***

### getChildren

Returns an array with all the child nodes.

```php
public getChildren(): \Sabre\DAV\INode[]
```












***

### createFile

Creates a new file in the directory.

```php
public createFile(string $name, resource|string $data = null): string|null
```

Data will either be supplied as a stream resource, or in certain cases
as a string. Keep in mind that you may have to support either.

After successful creation of the file, you may choose to return the ETag
of the new file here.

The returned ETag must be surrounded by double-quotes (The quotes should
be part of the actual string).

If you cannot accurately determine the ETag, you should not return it.
If you don't store the file exactly as-is (you're transforming it
somehow) you should also not return an ETag.

This means that if a subsequent GET to this new file does not exactly
return the same contents of what was submitted here, you are strongly
recommended to omit the ETag.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Name of the file |
| `$data` | **resource&#124;string** | Initial payload |





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

### calendarQuery

Performs a calendar-query on the contents of this calendar.

```php
public calendarQuery(array $filters): array
```

The calendar-query is defined in RFC4791 : CalDAV. Using the
calendar-query it is possible for a client to request a specific set of
object, based on contents of iCalendar properties, date-ranges and
iCalendar component types (VTODO, VEVENT).

This method should just return a list of (relative) urls that match this
query.

The list of filters are specified as an array. The exact array is
documented by \Sabre\CalDAV\CalendarQueryParser.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filters` | **array** |  |





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

- [`Forbidden`](../../DAV/Exception/Forbidden.md)



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

### getChild

Returns a child object, by its name.

```php
public getChild(string $name): \Sabre\DAV\INode
```

This method makes use of the getChildren method to grab all the child
nodes, and compares the name.
Generally its wise to override this, as this can usually be optimized

This method must throw Sabre\DAV\Exception\NotFound if the node does not
exist.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`NotFound`](../../DAV/Exception/NotFound.md)



***

### childExists

Checks is a child-node exists.

```php
public childExists(string $name): bool
```

It is generally a good idea to try and override this. Usually it can be optimized.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### createFile

Creates a new file in the directory.

```php
public createFile(string $name, resource|string $data = null): string|null
```

Data will either be supplied as a stream resource, or in certain cases
as a string. Keep in mind that you may have to support either.

After successful creation of the file, you may choose to return the ETag
of the new file here.

The returned ETag must be surrounded by double-quotes (The quotes should
be part of the actual string).

If you cannot accurately determine the ETag, you should not return it.
If you don't store the file exactly as-is (you're transforming it
somehow) you should also not return an ETag.

This means that if a subsequent GET to this new file does not exactly
return the same contents of what was submitted here, you are strongly
recommended to omit the ETag.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Name of the file |
| `$data` | **resource&#124;string** | Initial payload |





***

### createDirectory

Creates a new subdirectory.

```php
public createDirectory(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`Forbidden`](../../DAV/Exception/Forbidden.md)



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
