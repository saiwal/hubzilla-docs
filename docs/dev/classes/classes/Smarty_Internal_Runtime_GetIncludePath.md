
# Smarty_Internal_Runtime_GetIncludePath

Smarty Internal Read Include Path Class



* Full name: `\Smarty_Internal_Runtime_GetIncludePath`



## Properties


### _include_path

include path cache

```php
public string $_include_path
```






***

### _include_dirs

include path directory cache

```php
public array $_include_dirs
```






***

### _user_dirs

include path directory cache

```php
public array $_user_dirs
```






***

### isFile

stream cache

```php
public string[][] $isFile
```






***

### isPath

stream cache

```php
public string[] $isPath
```






***

### number

stream cache

```php
public int[] $number
```






***

### _has_stream_include

status cache

```php
public bool $_has_stream_include
```






***

### counter

Number for array index

```php
public int $counter
```






***

## Methods


### isNewIncludePath

Check if include path was updated

```php
public isNewIncludePath(\Smarty $smarty): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |





***

### getIncludePathDirs

return array with include path directories

```php
public getIncludePathDirs(\Smarty $smarty): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |





***

### getIncludePath

Return full file path from PHP include_path

```php
public getIncludePath(string[] $dirs, string $file, \Smarty $smarty): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dirs` | **string[]** |  |
| `$file` | **string** |  |
| `$smarty` | **\Smarty** |  |


**Return Value:**

full filepath or false




***


***
> Automatically generated on 2025-03-15
