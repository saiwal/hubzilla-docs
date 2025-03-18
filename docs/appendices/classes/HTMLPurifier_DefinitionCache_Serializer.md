
# HTMLPurifier_DefinitionCache_Serializer

Abstract class representing Definition cache managers that implements
useful common methods and is a factory.



* Full name: `\HTMLPurifier_DefinitionCache_Serializer`
* Parent class: [`\HTMLPurifier_DefinitionCache`](./HTMLPurifier_DefinitionCache.md)




## Methods


### add

Adds a definition object to the cache

```php
public add(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): int|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### set

Unconditionally saves a definition object to the cache

```php
public set(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): int|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### replace

Replace an object in the cache

```php
public replace(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): int|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### get

Retrieves a definition object from the cache

```php
public get(\HTMLPurifier_Config $config): bool|\HTMLPurifier_Config
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### remove

Removes a definition object to the cache

```php
public remove(\HTMLPurifier_Config $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### flush

Clears all objects from cache

```php
public flush(\HTMLPurifier_Config $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### cleanup

Clears all expired (older version or revision) objects from cache

```php
public cleanup(\HTMLPurifier_Config $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### generateFilePath

Generates the file path to the serial file corresponding to
the configuration and definition name

```php
public generateFilePath(\HTMLPurifier_Config $config): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### generateDirectoryPath

Generates the path to the directory contain this cache's serial files

```php
public generateDirectoryPath(\HTMLPurifier_Config $config): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### generateBaseDirectoryPath

Generates path to base directory that contains all definition type
serials

```php
public generateBaseDirectoryPath(\HTMLPurifier_Config $config): mixed|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### _write

Convenience wrapper function for file_put_contents

```php
private _write(string $file, string $data, \HTMLPurifier_Config $config): int|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** | File name to write to |
| `$data` | **string** | Data to write into file |
| `$config` | **\HTMLPurifier_Config** |  |


**Return Value:**

Number of bytes written if success, or false if failure.




***

### _prepareDir

Prepares the directory that this type stores the serials in

```php
private _prepareDir(\HTMLPurifier_Config $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |


**Return Value:**

True if successful




***

### _testPermissions

Tests permissions on a directory and throws out friendly
error messages and attempts to chmod it itself if possible

```php
private _testPermissions(string $dir, int $chmod): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** | Directory path |
| `$chmod` | **int** | Permissions |


**Return Value:**

True if directory is writable




***


## Inherited methods


### __construct



```php
public __construct(string $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | Type of definition objects this instance of the<br />cache will handle. |





***

### generateKey

Generates a unique identifier for a particular configuration

```php
public generateKey(\HTMLPurifier_Config $config): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** | Instance of HTMLPurifier_Config |





***

### isOld

Tests whether or not a key is old with respect to the configuration's
version and revision number.

```php
public isOld(string $key, \HTMLPurifier_Config $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | Key to test |
| `$config` | **\HTMLPurifier_Config** | Instance of HTMLPurifier_Config to test against |





***

### checkDefType

Checks if a definition's type jives with the cache's type

```php
public checkDefType(\HTMLPurifier_Definition $def): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** | Definition object to check |


**Return Value:**

true if good, false if not




***

### add

Adds a definition object to the cache

```php
public add(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### set

Unconditionally saves a definition object to the cache

```php
public set(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### replace

Replace an object in the cache

```php
public replace(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### get

Retrieves a definition object from the cache

```php
public get(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### remove

Removes a definition object to the cache

```php
public remove(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### flush

Clears all objects from cache

```php
public flush(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### cleanup

Clears all expired (older version or revision) objects from cache

```php
public cleanup(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


***
> Automatically generated on 2025-03-18
