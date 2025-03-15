
# Directory





* Full name: `\Zotlabs\Storage\Directory`
* Parent class: [`Node`](../../Sabre/DAV/Node.md)
* This class implements:
[`\Sabre\DAV\ICollection`](../../Sabre/DAV/ICollection.md), [`\Sabre\DAV\IQuota`](../../Sabre/DAV/IQuota.md), [`\Sabre\DAV\IMoveTarget`](../../Sabre/DAV/IMoveTarget.md)

**See Also:**

* http://github.com/friendica/red - 



## Properties


### red_path



```php
private string $red_path
```






***

### folder_hash



```php
public $folder_hash
```






***

### data



```php
public $data
```






***

### ext_path



```php
private string $ext_path
```






***

### root_dir



```php
private $root_dir
```






***

### auth



```php
private $auth
```






***

### os_path



```php
public string $os_path
```






***

## Methods


### __construct



```php
public __construct(string $ext_path, mixed $data, \Zotlabs\Storage\BasicAuth& $auth_plugin): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ext_path` | **string** | a full path |
| `$data` | **mixed** |  |
| `$auth_plugin` | **\Zotlabs\Storage\BasicAuth** |  |





***

### log



```php
private log(): mixed
```












***

### getChildren



```php
public getChildren(): array
```









**Return Value:**

\\Sabre\\DAV\\INode[]



**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)



***

### getChild



```php
public getChild(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)

- [`&quot;\Sabre\DAV\Exception\NotFound&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/NotFound&amp;amp;quot;.md)



***

### getName



```php
public getName(): string
```












***

### setName



```php
public setName(string $name): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | The new name of the directory. |




**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)



***

### createFile



```php
public createFile(string $name, resource|string $data = null): null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Name of the file |
| `$data` | **resource&#124;string** | Initial payload |


**Return Value:**

ETag



**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)



***

### createDirectory



```php
public createDirectory(string $name): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | the directory to create |





***

### delete



```php
public delete(): mixed
```












***

### childExists



```php
public childExists(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | <br />The name to check if it exists. |





***

### moveInto



```php
public moveInto(mixed $targetName, mixed $sourcePath, \Sabre\DAV\INode $sourceNode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$targetName` | **mixed** |  |
| `$sourcePath` | **mixed** |  |
| `$sourceNode` | **\Sabre\DAV\INode** |  |





***

### getDir



```php
public getDir(): void
```











**Throws:**

- [`&quot;\Sabre\DAV\Exception\NotFound&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/NotFound&amp;amp;quot;.md)



***

### getLastModified



```php
public getLastModified(): int
```









**Return Value:**

last modification time in UNIX timestamp




***

### CollectionData



```php
public CollectionData(string $file, \Zotlabs\Storage\BasicAuth& $auth): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** | path to a directory |
| `$auth` | **\Zotlabs\Storage\BasicAuth** |  |




**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)

- [`&quot;\Sabre\DAV\Exception\NotFound&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/NotFound&amp;amp;quot;.md)



***

### ChannelList



```php
public ChannelList(\Zotlabs\Storage\BasicAuth& $auth): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$auth` | **\Zotlabs\Storage\BasicAuth** |  |


**Return Value:**

Directory[]




***

### FileData



```php
public FileData(string $file, \Zotlabs\Storage\BasicAuth& $auth, bool $test = false): \Zotlabs\Storage\File|\Zotlabs\Storage\Directory|bool|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** | <br />path to file or directory |
| `$auth` | **\Zotlabs\Storage\BasicAuth** |  |
| `$test` | **bool** | (optional) enable test mode |




**Throws:**

- [`&quot;\Sabre\DAV\Exception\Forbidden&quot;`](../../../classes&amp;amp;quot;/Sabre/DAV/Exception/Forbidden&amp;amp;quot;.md)



***

### getQuotaInfo



```php
public getQuotaInfo(): mixed
```












***


***
> Automatically generated on 2025-03-15
