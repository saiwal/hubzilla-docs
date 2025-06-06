
# IPatchSupport

This interface provides a way to modify only part of a target resource
It may be used to update a file chunk, upload big a file into smaller
chunks or resume an upload.



* Full name: `\Sabre\DAV\PartialUpdate\IPatchSupport`
* Parent interfaces: [`\Sabre\DAV\IFile`](../IFile.md)


## Methods


### patch

Updates the file based on a range specification.

```php
public patch(resource|string $data, int $rangeType, int $offset = null): string|null
```

The first argument is the data, which is either a readable stream
resource or a string.

The second argument is the type of update we're doing.
This is either:
* 1. append
* 2. update based on a start byte
* 3. update based on an end byte
;
The third argument is the start or end byte.

After a successful put operation, you may choose to return an ETag. The
etag must always be surrounded by double-quotes. These quotes must
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

### put

Replaces the contents of the file.

```php
public put(resource|string $data): string|null
```

The data argument is a readable stream resource.

After a successful put operation, you may choose to return an ETag. The
etag must always be surrounded by double-quotes. These quotes must
appear in the actual string you're returning.

Clients may use the ETag from a PUT request to later on make sure that
when they update the file, the contents haven't changed in the mean
time.

If you don't plan to store the file byte-by-byte, and you return a
different object on a subsequent GET you are strongly recommended to not
return an ETag, and just return null.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource&#124;string** |  |





***

### get

Returns the data.

```php
public get(): mixed
```

This method may either return a string or a readable stream resource










***

### getContentType

Returns the mime-type for a file.

```php
public getContentType(): string|null
```

If null is returned, we'll assume application/octet-stream










***

### getETag

Returns the ETag for a file.

```php
public getETag(): string|null
```

An ETag is a unique identifier representing the current version of the file. If the file changes, the ETag MUST change.

Return null if the ETag can not effectively be determined.

The ETag must be surrounded by double-quotes, so something like this
would make a valid ETag:

  return '"someetag"';










***

### getSize

Returns the size of the node, in bytes.

```php
public getSize(): int
```












***


***
> Automatically generated on 2025-03-18
