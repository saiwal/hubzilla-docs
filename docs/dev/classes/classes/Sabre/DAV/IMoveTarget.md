
# IMoveTarget

By implementing this interface, a collection can effectively say "other
nodes may be moved into this collection".

The benefit of this, is that sabre/dav will by default perform a move, by
transferring an entire directory tree, copying every collection, and deleting
every item.

If a backend supports a better optimized move operation, this can trigger
some huge speed gains.

* Full name: `\Sabre\DAV\IMoveTarget`
* Parent interfaces: [`\Sabre\DAV\ICollection`](./ICollection.md)


## Methods


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
> Automatically generated on 2025-03-15
