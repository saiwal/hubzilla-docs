***

# SimpleCollection

SimpleCollection.

The SimpleCollection is used to quickly setup static directory structures.
Just create the object with a proper name, and add children to use it.

* Full name: `\Sabre\DAV\SimpleCollection`
* Parent class: [`\Sabre\DAV\Collection`](./Collection.md)



## Properties


### children

List of childnodes.

```php
protected \Sabre\DAV\INode[] $children
```






***

### name

Name of this resource.

```php
protected string $name
```






***

## Methods


### __construct

Creates this node.

```php
public __construct(string $name, \Sabre\DAV\INode[] $children = []): mixed
```

The name of the node must be passed, child nodes can also be passed.
This nodes must be instances of INode






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$children` | **\Sabre\DAV\INode[]** |  |





***

### addChild

Adds a new childnode to this collection.

```php
public addChild(\Sabre\DAV\INode $child): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$child` | **\Sabre\DAV\INode** |  |





***

### getName

Returns the name of the collection.

```php
public getName(): string
```












***

### getChild

Returns a child object, by its name.

```php
public getChild(string $name): \Sabre\DAV\INode
```

This method makes use of the getChildren method to grab all the child nodes, and compares the name.
Generally its wise to override this, as this can usually be optimized

This method must throw Sabre\DAV\Exception\NotFound if the node does not
exist.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`NotFound`](./Exception/NotFound.md)



***

### getChildren

Returns a list of children for this collection.

```php
public getChildren(): \Sabre\DAV\INode[]
```












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

- [`Forbidden`](./Exception/Forbidden.md)



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

- [`Forbidden`](./Exception/Forbidden.md)



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

- [`NotFound`](./Exception/NotFound.md)



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

- [`Forbidden`](./Exception/Forbidden.md)



***


***
> Automatically generated on 2025-03-15
