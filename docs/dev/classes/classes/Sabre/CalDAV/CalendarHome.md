***

# CalendarHome

The CalendarHome represents a node that is usually in a users'
calendar-homeset.

It contains all the users' calendars, and can optionally contain a
notifications collection, calendar subscriptions, a users' inbox, and a
users' outbox.

* Full name: `\Sabre\CalDAV\CalendarHome`
* This class implements:
[`\Sabre\DAV\IExtendedCollection`](../DAV/IExtendedCollection.md), [`\Sabre\DAVACL\IACL`](../DAVACL/IACL.md)



## Properties


### caldavBackend

CalDAV backend.

```php
protected \Sabre\CalDAV\Backend\BackendInterface $caldavBackend
```






***

### principalInfo

Principal information.

```php
protected array $principalInfo
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CalDAV\Backend\BackendInterface $caldavBackend, array $principalInfo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caldavBackend` | **\Sabre\CalDAV\Backend\BackendInterface** |  |
| `$principalInfo` | **array** |  |





***

### getName

Returns the name of this object.

```php
public getName(): string
```












***

### setName

Updates the name of this object.

```php
public setName(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### delete

Deletes this object.

```php
public delete(): mixed
```












***

### getLastModified

Returns the last modification date.

```php
public getLastModified(): int
```












***

### createFile

Creates a new file under this object.

```php
public createFile(string $name, resource $data = null): string|null
```

This is currently not allowed






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$data` | **resource** |  |





***

### createDirectory

Creates a new directory under this object.

```php
public createDirectory(string $filename): mixed
```

This is currently not allowed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |





***

### getChild

Returns a single calendar, by name.

```php
public getChild(string $name): \Sabre\CalDAV\Calendar
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### childExists

Checks if a calendar exists.

```php
public childExists(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getChildren

Returns a list of calendars.

```php
public getChildren(): array
```












***

### createExtendedCollection

Creates a new calendar or subscription.

```php
public createExtendedCollection(string $name, \Sabre\DAV\MkCol $mkCol): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$mkCol` | **\Sabre\DAV\MkCol** |  |




**Throws:**

- [`InvalidResourceType`](../DAV/Exception/InvalidResourceType.md)



***

### getOwner

Returns the owner of the calendar home.

```php
public getOwner(): string
```












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

### shareReply

This method is called when a user replied to a request to share.

```php
public shareReply(string $href, int $status, string $calendarUri, string $inReplyTo, string $summary = null): string|null
```

This method should return the url of the newly created calendar if the
share was accepted.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$href` | **string** | The sharee who is replying (often a mailto: address) |
| `$status` | **int** | One of the SharingPlugin::STATUS_* constants |
| `$calendarUri` | **string** | The url to the calendar thats being shared |
| `$inReplyTo` | **string** | The unique id this message is a response to |
| `$summary` | **string** | A description of the reply |





***

### getCalendarObjectByUID

Searches through all of a users calendars and calendar objects to find
an object with a specific UID.

```php
public getCalendarObjectByUID(string $uid): string|null
```

This method should return the path to this object, relative to the
calendar home, so this path usually only contains two parts:

calendarpath/objectpath.ics

If the uid is not found, return null.

This method should only consider * objects that the principal owns, so
any calendars owned by other principals that also appear in this
collection should be ignored.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **string** |  |





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
> Automatically generated on 2025-03-15
