
# Calendar

This object represents a CalDAV calendar.

A calendar can contain multiple TODO and or Events. These are represented
as \Sabre\CalDAV\CalendarObject objects.

* Full name: `\Sabre\CalDAV\Calendar`
* This class implements:
[`\Sabre\CalDAV\ICalendar`](./ICalendar.md), [`\Sabre\DAV\IProperties`](../DAV/IProperties.md), [`\Sabre\DAV\Sync\ISyncCollection`](../DAV/Sync/ISyncCollection.md), [`\Sabre\DAV\IMultiGet`](../DAV/IMultiGet.md)



## Properties


### calendarInfo

This is an array with calendar information.

```php
protected array $calendarInfo
```






***

### caldavBackend

CalDAV backend.

```php
protected \Sabre\CalDAV\Backend\BackendInterface $caldavBackend
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CalDAV\Backend\BackendInterface $caldavBackend, array $calendarInfo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caldavBackend` | **\Sabre\CalDAV\Backend\BackendInterface** |  |
| `$calendarInfo` | **array** |  |





***

### getName

Returns the name of the calendar.

```php
public getName(): string
```












***

### propPatch

Updates properties on this node.

```php
public propPatch(\Sabre\DAV\PropPatch $propPatch): mixed
```

This method received a PropPatch object, which contains all the
information about the update.

To update specific properties, call the 'handle' method on this object.
Read the PropPatch documentation for more information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### getProperties

Returns the list of properties.

```php
public getProperties(array $requestedProperties): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$requestedProperties` | **array** |  |





***

### getChild

Returns a calendar object.

```php
public getChild(string $name): \Sabre\CalDAV\ICalendarObject
```

The contained calendar objects are for example Events or Todo's.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getChildren

Returns the full list of calendar objects.

```php
public getChildren(): array
```












***

### getMultipleChildren

This method receives a list of paths in it's first argument.

```php
public getMultipleChildren(string[] $paths): array
```

It must return an array with Node objects.

If any children are not found, you do not have to return them.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$paths` | **string[]** |  |





***

### childExists

Checks if a child-node exists.

```php
public childExists(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### createDirectory

Creates a new directory.

```php
public createDirectory(string $name): mixed
```

We actually block this, as subdirectories are not allowed in calendars.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### createFile

Creates a new file.

```php
public createFile(string $name, resource $data = null): string|null
```

The contents of the new file must be a valid ICalendar string.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$data` | **resource** |  |





***

### delete

Deletes the calendar.

```php
public delete(): mixed
```












***

### setName

Renames the calendar. Note that most calendars use the
{DAV:}displayname to display a name to display a name.

```php
public setName(string $newName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$newName` | **string** |  |





***

### getLastModified

Returns the last modification date as a unix timestamp.

```php
public getLastModified(): int|null
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

### getChildACL

This method returns the ACL's for calendar objects in this calendar.

```php
public getChildACL(): array
```

The result of this method automatically gets passed to the
calendar-object nodes in the calendar.










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
documented by Sabre\CalDAV\CalendarQueryParser.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filters` | **array** |  |





***

### getSyncToken

This method returns the current sync-token for this collection.

```php
public getSyncToken(): string|null
```

This can be any string.

If null is returned from this function, the plugin assumes there's no
sync information available.










***

### getChanges

The getChanges method returns all the changes that have happened, since
the specified syncToken and the current collection.

```php
public getChanges(string $syncToken, int $syncLevel, int $limit = null): array|null
```

This function should return an array, such as the following:

[
  'syncToken' => 'The current synctoken',
  'added'   => [
     'new.txt',
  ],
  'modified'   => [
     'modified.txt',
  ],
  'deleted' => [
     'foo.php.bak',
     'old.txt'
  ],
  'result_truncated' : true
];

The syncToken property should reflect the *current* syncToken of the
collection, as reported getSyncToken(). This is needed here too, to
ensure the operation is atomic.

If the syncToken is specified as null, this is an initial sync, and all
members should be reported.

If result is truncated due to server limitation or limit by client,
set result_truncated to true, otherwise set to false or do not add the key.

The modified property is an array of nodenames that have changed since
the last token.

The deleted property is an array with nodenames, that have been deleted
from collection.

The second argument is basically the 'depth' of the report. If it's 1,
you only have to report changes that happened only directly in immediate
descendants. If it's 2, it should also include changes from the nodes
below the child collections. (grandchildren)

The third (optional) argument allows a client to specify how many
results should be returned at most. If the limit is not specified, it
should be treated as infinite.

If the limit (infinite or not) is higher than you're willing to return,
the result should be truncated to fit the limit.
Note that even when the result is truncated, syncToken must be consistent
with the truncated result, not the result before truncation.
(See RFC6578 Section 3.6 for detail)

If the syncToken is expired (due to data cleanup) or unknown, you must
return null.

The limit is 'suggestive'. You are free to ignore it.
TODO: RFC6578 Setion 3.7 says that the server must fail when the server
cannot truncate according to the limit, so it may not be just suggestive.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$syncToken` | **string** |  |
| `$syncLevel` | **int** |  |
| `$limit` | **int** |  |





***


## Inherited methods


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
> Automatically generated on 2025-03-18
