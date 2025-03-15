
# Collection

This is an ACL-enabled collection.



* Full name: `\Sabre\DAVACL\FS\Collection`
* Parent class: [`\Sabre\DAV\FSExt\Directory`](../../DAV/FSExt/Directory.md)
* This class implements:
[`\Sabre\DAVACL\IACL`](../IACL.md)



## Properties


### acl

A list of ACL rules.

```php
protected array $acl
```






***

### owner

Owner uri, or null for no owner.

```php
protected string|null $owner
```






***

## Methods


### __construct

Constructor.

```php
public __construct(string $path, array $acl, string|null $owner = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** | on-disk path |
| `$acl` | **array** | ACL rules |
| `$owner` | **string&#124;null** | principal owner string |





***

### getChild

Returns a specific child node, referenced by its name.

```php
public getChild(string $name): \Sabre\DAV\INode
```

This method must throw Sabre\DAV\Exception\NotFound if the node does not
exist.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`NotFound`](../../DAV/Exception/NotFound.md)



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


### __construct

Sets up the node, expects a full path name.

```php
public __construct(string $path, string $overrideName = null): mixed
```

If $overrideName is set, this node shows up in the tree under a
different name. In this case setName() will be disabled.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$overrideName` | **string** |  |





***

### getName

Returns the name of the node.

```php
public getName(): string
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





***

### getLastModified

Returns the last modification time, as a unix timestamp.

```php
public getLastModified(): int
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

### createDirectory

Creates a new subdirectory.

```php
public createDirectory(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getChild

Returns a specific child node, referenced by its name.

```php
public getChild(string $name): \Sabre\DAV\INode
```

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

Checks if a child exists.

```php
public childExists(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getChildren

Returns an array with all the child nodes.

```php
public getChildren(): \Sabre\DAV\INode[]
```












***

### delete

Deletes all files in this directory, and then itself.

```php
public delete(): bool
```












***

### getQuotaInfo

Returns available diskspace information.

```php
public getQuotaInfo(): array
```












***

### moveInto

Moves a node into this collection.

```php
public moveInto(string $targetName, string $sourcePath, \Sabre\DAV\INode $sourceNode): bool
```

It is up to the implementors to:
  1. Create the new resource.
  2. Remove the old resource.
  3. Transfer any properties or other data.

Generally you should make very sure that your collection can easily move
the move.

If you don't, just return false, which will trigger sabre/dav to handle
the move itself. If you return true from this function, the assumption
is that the move was successful.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$targetName` | **string** | new local file/collection name |
| `$sourcePath` | **string** | Full path to source node |
| `$sourceNode` | **\Sabre\DAV\INode** | Source node itself |





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
