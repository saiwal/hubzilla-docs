
# Node

Base node-class.

The node class implements the method used by both the File and the Directory classes

* Full name: `\Sabre\DAV\FS\Node`
* This class implements:
[`\Sabre\DAV\INode`](../INode.md)
* This class is an **Abstract class**



## Properties


### path

The path to the current node.

```php
protected string $path
```






***

### overrideName

The overridden name of the node.

```php
protected string $overrideName
```






***

## Methods


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


***
> Automatically generated on 2025-03-18
