***

# File

File class.

This is a helper class, that should aid in getting file classes setup.
Most of its methods are implemented, and throw permission denied exceptions

* Full name: `\Sabre\DAV\File`
* Parent class: [`\Sabre\DAV\Node`](./Node.md)
* This class implements:
[`\Sabre\DAV\IFile`](./IFile.md)
* This class is an **Abstract class**




## Methods


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


***
> Automatically generated on 2025-03-15
