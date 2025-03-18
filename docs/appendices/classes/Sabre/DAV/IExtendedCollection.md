
# IExtendedCollection

The IExtendedCollection interface.

This interface can be used to create special-type of collection-resources
as defined by RFC 5689.

* Full name: `\Sabre\DAV\IExtendedCollection`
* Parent interfaces: [`\Sabre\DAV\ICollection`](./ICollection.md)


## Methods


### createExtendedCollection

Creates a new collection.

```php
public createExtendedCollection(string $name, \Sabre\DAV\MkCol $mkCol): mixed
```

This method will receive a MkCol object with all the information about
the new collection that's being created.

The MkCol object contains information about the resourceType of the new
collection. If you don't support the specified resourceType, you should
throw Exception\InvalidResourceType.

The object also contains a list of WebDAV properties for the new
collection.

You should call the handle() method on this object to specify exactly
which properties you are storing. This allows the system to figure out
exactly which properties you didn't store, which in turn allows other
plugins (such as the propertystorage plugin) to handle storing the
property for you.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$mkCol` | **\Sabre\DAV\MkCol** |  |




**Throws:**

- [`InvalidResourceType`](./Exception/InvalidResourceType.md)



***


## Inherited methods


### delete

Deleted the current node.

```php
public delete(): mixed
```












***

### getName

Returns the name of the node.

```php
public getName(): string
```

This is used to generate the url.










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

Returns the last modification time, as a unix timestamp. Return null
if the information is not available.

```php
public getLastModified(): int|null
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





***

### getChildren

Returns an array with all the child nodes.

```php
public getChildren(): \Sabre\DAV\INode[]
```












***

### childExists

Checks if a child-node with the specified name exists.

```php
public childExists(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***


***
> Automatically generated on 2025-03-18
