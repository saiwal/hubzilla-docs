***

# AddressBookHome

AddressBook Home class.

This collection contains a list of addressbooks associated with one user.

* Full name: `\Sabre\CardDAV\AddressBookHome`
* Parent class: [`\Sabre\DAV\Collection`](../DAV/Collection.md)
* This class implements:
[`\Sabre\DAV\IExtendedCollection`](../DAV/IExtendedCollection.md), [`\Sabre\DAVACL\IACL`](../DAVACL/IACL.md)



## Properties


### principalUri

Principal uri.

```php
protected array $principalUri
```






***

### carddavBackend

carddavBackend.

```php
protected \Sabre\CardDAV\Backend\BackendInterface $carddavBackend
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CardDAV\Backend\BackendInterface $carddavBackend, string $principalUri): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$carddavBackend` | **\Sabre\CardDAV\Backend\BackendInterface** |  |
| `$principalUri` | **string** |  |





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

Returns a single addressbook, by name.

```php
public getChild(string $name): \Sabre\CardDAV\AddressBook
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getChildren

Returns a list of addressbooks.

```php
public getChildren(): array
```












***

### createExtendedCollection

Creates a new address book.

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

- [`NotFound`](../DAV/Exception/NotFound.md)



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

- [`Forbidden`](../DAV/Exception/Forbidden.md)



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
