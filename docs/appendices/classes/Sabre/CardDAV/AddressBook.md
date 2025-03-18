
# AddressBook

The AddressBook class represents a CardDAV addressbook, owned by a specific user.

The AddressBook can contain multiple vcards

* Full name: `\Sabre\CardDAV\AddressBook`
* Parent class: [`\Sabre\DAV\Collection`](../DAV/Collection.md)
* This class implements:
[`\Sabre\CardDAV\IAddressBook`](./IAddressBook.md), [`\Sabre\DAV\IProperties`](../DAV/IProperties.md), [`\Sabre\DAVACL\IACL`](../DAVACL/IACL.md), [`\Sabre\DAV\Sync\ISyncCollection`](../DAV/Sync/ISyncCollection.md), [`\Sabre\DAV\IMultiGet`](../DAV/IMultiGet.md)



## Properties


### addressBookInfo

This is an array with addressbook information.

```php
protected array $addressBookInfo
```






***

### carddavBackend

CardDAV backend.

```php
protected \Sabre\CardDAV\Backend\BackendInterface $carddavBackend
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\CardDAV\Backend\BackendInterface $carddavBackend, array $addressBookInfo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$carddavBackend` | **\Sabre\CardDAV\Backend\BackendInterface** |  |
| `$addressBookInfo` | **array** |  |





***

### getName

Returns the name of the addressbook.

```php
public getName(): string
```












***

### getChild

Returns a card.

```php
public getChild(string $name): \Sabre\CardDAV\Card
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getChildren

Returns the full list of cards.

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

### createDirectory

Creates a new directory.

```php
public createDirectory(string $name): mixed
```

We actually block this, as subdirectories are not allowed in addressbooks.






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

The contents of the new file must be a valid VCARD.

This method may return an ETag.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$data` | **resource** |  |





***

### delete

Deletes the entire addressbook.

```php
public delete(): mixed
```












***

### setName

Renames the addressbook.

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
public getLastModified(): int
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

Returns a list of properties for this nodes.

```php
public getProperties(array $properties): array
```

The properties list is a list of propertynames the client requested,
encoded in clark-notation {xmlnamespace}tagname

If the array is empty, it means 'all properties' were requested.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **array** |  |





***

### getOwner

Returns the owner principal.

```php
public getOwner(): string|null
```

This must be a url to a principal, or null if there's no owner










***

### getChildACL

This method returns the ACL's for card nodes in this address book.

```php
public getChildACL(): array
```

The result of this method automatically gets passed to the
card nodes in this address book.










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
  ]
];

The syncToken property should reflect the *current* syncToken of the
collection, as reported getSyncToken(). This is needed here too, to
ensure the operation is atomic.

If the syncToken is specified as null, this is an initial sync, and all
members should be reported.

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
you should throw a Sabre\DAV\Exception\TooMuchMatches() exception.

If the syncToken is expired (due to data cleanup) or unknown, you must
return null.

The limit is 'suggestive'. You are free to ignore it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$syncToken` | **string** |  |
| `$syncLevel` | **int** |  |
| `$limit` | **int** |  |





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
> Automatically generated on 2025-03-18
