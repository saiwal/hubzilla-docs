***

# File

Node class.



* Full name: `\Zotlabs\Storage\File`
* Parent class: [`\Sabre\DAV\Node`](../../Sabre/DAV/Node.md)
* This class implements:
[`\Sabre\DAV\IFile`](../../Sabre/DAV/IFile.md)

**See Also:**

* http://github.com/friendica/red - 



## Properties


### data

The file from attach table.

```php
public array $data
```






***

### auth



```php
private $auth
```





**See Also:**

*  - \\Sabre\\DAV\\Auth\\Backend\\BackendInterface

***

### name



```php
private string $name
```






***

### os_path



```php
public $os_path
```






***

### folder_hash



```php
public $folder_hash
```






***

## Methods


### __construct

Sets up the node, expects a full path name.

```php
public __construct(string $name, array $data, mixed& $auth): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$data` | **array** | from attach table |
| `$auth` | **mixed** |  |





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
public setName(string $newName): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$newName` | **string** | The new name of the file. |




**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)



***

### put

Replaces the contents of the file.

```php
public put(resource $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource** |  |





***

### get

Returns the data.

```php
public get(): string
```












***

### getETag

Returns the ETag for a file.

```php
public getETag(): null|string
```












***

### getContentType

Returns the mime-type for a file.

```php
public getContentType(): mixed
```












***

### getSize

Returns the size of the node, in bytes.

```php
public getSize(): int
```









**Return Value:**


filesize in bytes




***

### getLastModified

Returns the last modification time as a unix timestamp.

```php
public getLastModified(): int
```









**Return Value:**

last modification time in UNIX timestamp




***

### delete

Deletes the current node.

```php
public delete(): mixed
```











**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)



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

- [`Forbidden`](../../Sabre/DAV/Exception/Forbidden.md)



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

- [`Forbidden`](../../Sabre/DAV/Exception/Forbidden.md)



***


***
> Automatically generated on 2025-03-15
