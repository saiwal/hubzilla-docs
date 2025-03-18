
# File

File class.



* Full name: `\Sabre\DAV\FS\File`
* Parent class: [`\Sabre\DAV\FS\Node`](./Node.md)
* This class implements:
[`\Sabre\DAV\IFile`](../IFile.md)




## Methods


### put

Updates the data.

```php
public put(resource $data): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource** |  |





***

### get

Returns the data.

```php
public get(): resource
```












***

### delete

Delete the current file.

```php
public delete(): mixed
```












***

### getSize

Returns the size of the node, in bytes.

```php
public getSize(): int
```












***

### getETag

Returns the ETag for a file.

```php
public getETag(): mixed
```

An ETag is a unique identifier representing the current version of the file. If the file changes, the ETag MUST change.
The ETag is an arbitrary string, but MUST be surrounded by double-quotes.

Return null if the ETag can not effectively be determined










***

### getContentType

Returns the mime-type for a file.

```php
public getContentType(): mixed
```

If null is returned, we'll assume application/octet-stream










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


***
> Automatically generated on 2025-03-18
