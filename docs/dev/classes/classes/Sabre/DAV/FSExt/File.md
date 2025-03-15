
# File

File class.



* Full name: `\Sabre\DAV\FSExt\File`
* Parent class: [`\Sabre\DAV\FS\Node`](../FS/Node.md)
* This class implements:
[`\Sabre\DAV\PartialUpdate\IPatchSupport`](../PartialUpdate/IPatchSupport.md)




## Methods


### put

Updates the data.

```php
public put(resource|string $data): string
```

Data is a readable stream resource.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource&#124;string** |  |





***

### patch

Updates the file based on a range specification.

```php
public patch(resource|string $data, int $rangeType, int $offset = null): string|null
```

The first argument is the data, which is either a readable stream
resource or a string.

The second argument is the type of update we're doing.
This is either:
* 1. append (default)
* 2. update based on a start byte
* 3. update based on an end byte
;
The third argument is the start or end byte.

After a successful put operation, you may choose to return an ETag. The
ETAG must always be surrounded by double-quotes. These quotes must
appear in the actual string you're returning.

Clients may use the ETag from a PUT request to later on make sure that
when they update the file, the contents haven't changed in the mean
time.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource&#124;string** |  |
| `$rangeType` | **int** |  |
| `$offset` | **int** |  |





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
public delete(): bool
```












***

### getETag

Returns the ETag for a file.

```php
public getETag(): string|null
```

An ETag is a unique identifier representing the current version of the file. If the file changes, the ETag MUST change.
The ETag is an arbitrary string, but MUST be surrounded by double-quotes.

Return null if the ETag can not effectively be determined










***

### getContentType

Returns the mime-type for a file.

```php
public getContentType(): string|null
```

If null is returned, we'll assume application/octet-stream










***

### getSize

Returns the size of the file, in bytes.

```php
public getSize(): int
```












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
> Automatically generated on 2025-03-15
