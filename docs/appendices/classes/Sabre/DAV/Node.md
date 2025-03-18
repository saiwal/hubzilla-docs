
# Node

Node class.

This is a helper class, that should aid in getting nodes setup.

* Full name: `\Sabre\DAV\Node`
* This class implements:
[`\Sabre\DAV\INode`](./INode.md)
* This class is an **Abstract class**




## Methods


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


***
> Automatically generated on 2025-03-18
