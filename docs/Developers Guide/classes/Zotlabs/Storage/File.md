
# File





* Full name: `\Zotlabs\Storage\File`
* Parent class: [`Node`](../../Sabre/DAV/Node.md)
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



```php
public getName(): string
```












***

### setName



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



```php
public put(resource $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **resource** |  |





***

### get



```php
public get(): string
```












***

### getETag



```php
public getETag(): null|string
```












***

### getContentType



```php
public getContentType(): mixed
```












***

### getSize



```php
public getSize(): int
```









**Return Value:**


filesize in bytes




***

### getLastModified



```php
public getLastModified(): int
```









**Return Value:**

last modification time in UNIX timestamp




***

### delete



```php
public delete(): mixed
```











**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)



***


***
> Automatically generated on 2025-03-15
