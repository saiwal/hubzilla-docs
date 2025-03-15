
# Tree

The tree object is responsible for basic tree operations.

It allows for fetching nodes by path, facilitates deleting, copying and
moving.

* Full name: `\Sabre\DAV\Tree`
* This class implements:
[`\Sabre\DAV\INodeByPath`](./INodeByPath.md)



## Properties


### rootNode

The root node.

```php
protected \Sabre\DAV\ICollection $rootNode
```






***

### cache

This is the node cache. Accessed nodes are stored here.

```php
protected array $cache
```

Arrays keys are path names, values are the actual nodes.




***

## Methods


### __construct

Creates the object.

```php
public __construct(\Sabre\DAV\ICollection $rootNode): mixed
```

This method expects the rootObject to be passed as a parameter






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rootNode` | **\Sabre\DAV\ICollection** |  |





***

### getNodeForPath

Returns the INode object for the requested path.

```php
public getNodeForPath(string $path): \Sabre\DAV\INode
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### nodeExists

This function allows you to check if a node exists.

```php
public nodeExists(string $path): bool
```

Implementors of this class should override this method to make
it cheaper.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### copy

Copies a file from path to another.

```php
public copy(string $sourcePath, string $destinationPath): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sourcePath` | **string** | The source location |
| `$destinationPath` | **string** | The full destination path |





***

### move

Moves a file from one location to another.

```php
public move(string $sourcePath, string $destinationPath): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sourcePath` | **string** | The path to the file which should be moved |
| `$destinationPath` | **string** | The full destination path, so not just the destination parent node |





***

### delete

Deletes a node from the tree.

```php
public delete(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getChildren

Returns a list of childnodes for a given path.

```php
public getChildren(string $path): \Traversable
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### markDirty

This method is called with every tree update.

```php
public markDirty(string $path): mixed
```

Examples of tree updates are:
  * node deletions
  * node creations
  * copy
  * move
  * renaming nodes

If Tree classes implement a form of caching, this will allow
them to make sure caches will be expired.

If a path is passed, it is assumed that the entire subtree is dirty






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getMultipleNodes

This method tells the tree system to pre-fetch and cache a list of
children of a single parent.

```php
public getMultipleNodes(array $paths): array
```

There are a bunch of operations in the WebDAV stack that request many
children (based on uris), and sometimes fetching many at once can
optimize this.

This method returns an array with the found nodes. It's keys are the
original paths. The result may be out of order.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$paths` | **array** | list of nodes that must be fetched |





***

### copyNode

copyNode.

```php
protected copyNode(\Sabre\DAV\INode $source, \Sabre\DAV\ICollection $destinationParent, string $destinationName = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Sabre\DAV\INode** |  |
| `$destinationParent` | **\Sabre\DAV\ICollection** |  |
| `$destinationName` | **string** |  |





***


***
> Automatically generated on 2025-03-15
