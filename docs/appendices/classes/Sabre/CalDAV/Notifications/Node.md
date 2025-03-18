
# Node

This node represents a single notification.

The signature is mostly identical to that of Sabre\DAV\IFile, but the get() method
MUST return an xml document that matches the requirements of the
'caldav-notifications.txt' spec.

* Full name: `\Sabre\CalDAV\Notifications\Node`
* Parent class: [`\Sabre\DAV\File`](../../DAV/File.md)
* This class implements:
[`\Sabre\CalDAV\Notifications\INode`](./INode.md), [`\Sabre\DAVACL\IACL`](../../DAVACL/IACL.md)



## Properties


### caldavBackend

The notification backend.

```php
protected \Sabre\CalDAV\Backend\NotificationSupport $caldavBackend
```






***

### notification

The actual notification.

```php
protected \Sabre\CalDAV\Xml\Notification\NotificationInterface $notification
```






***

### principalUri

Owner principal of the notification.

```php
protected string $principalUri
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CalDAV\Backend\NotificationSupport $caldavBackend, string $principalUri, \Sabre\CalDAV\Xml\Notification\NotificationInterface $notification): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caldavBackend` | **\Sabre\CalDAV\Backend\NotificationSupport** |  |
| `$principalUri` | **string** |  |
| `$notification` | **\Sabre\CalDAV\Xml\Notification\NotificationInterface** |  |





***

### getName

Returns the path name for this notification.

```php
public getName(): string
```












***

### getETag

Returns the etag for the notification.

```php
public getETag(): string
```

The etag must be surrounded by litteral double-quotes.










***

### getNotificationType

This method must return an xml element, using the
Sabre\CalDAV\Xml\Notification\NotificationInterface classes.

```php
public getNotificationType(): \Sabre\CalDAV\Xml\Notification\NotificationInterface
```












***

### delete

Deletes this notification.

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
> Automatically generated on 2025-03-18
