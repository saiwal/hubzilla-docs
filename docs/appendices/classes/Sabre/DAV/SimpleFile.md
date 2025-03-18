
# SimpleFile

SimpleFile.

The 'SimpleFile' class is used to easily add read-only immutable files to
the directory structure. One usecase would be to add a 'readme.txt' to a
root of a webserver with some standard content.

* Full name: `\Sabre\DAV\SimpleFile`
* Parent class: [`\Sabre\DAV\File`](./File.md)



## Properties


### contents

File contents.

```php
protected string $contents
```






***

### name

Name of this resource.

```php
protected string $name
```






***

### mimeType

A mimetype, such as 'text/plain' or 'text/html'.

```php
protected string $mimeType
```






***

## Methods


### __construct

Creates this node.

```php
public __construct(string $name, string $contents, string|null $mimeType = null): mixed
```

The name of the node must be passed, as well as the contents of the
file.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$contents` | **string** |  |
| `$mimeType` | **string&#124;null** |  |





***

### getName

Returns the node name for this file.

```php
public getName(): string
```

This name is used to construct the url.










***

### get

Returns the data.

```php
public get(): mixed
```

This method may either return a string or a readable stream resource










***

### getSize

Returns the size of the file, in bytes.

```php
public getSize(): int
```












***

### getETag

Returns the ETag for a file.

```php
public getETag(): string
```

An ETag is a unique identifier representing the current version of the file. If the file changes, the ETag MUST change.
The ETag is an arbitrary string, but MUST be surrounded by double-quotes.

Return null if the ETag can not effectively be determined










***

### getContentType

Returns the mime-type for a file.

```php
public getContentType(): string
```

If null is returned, we'll assume application/octet-stream










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

### put

Replaces the contents of the file.

```php
public put(string|resource $data): string|null
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
| `$data` | **string&#124;resource** |  |





***

### get

Returns the data.

```php
public get(): mixed
```

This method may either return a string or a readable stream resource










***

### getSize

Returns the size of the file, in bytes.

```php
public getSize(): int
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


***
> Automatically generated on 2025-03-18
