***

# Smarty_Template_Cached

Smarty Resource Data Object
Cache Data Container for Template Files



* Full name: `\Smarty_Template_Cached`
* Parent class: [`\Smarty_Template_Resource_Base`](./Smarty_Template_Resource_Base.md)



## Properties


### valid

Cache Is Valid

```php
public bool $valid
```






***

### handler

CacheResource Handler

```php
public \Smarty_CacheResource $handler
```






***

### cache_id

Template Cache Id (Smarty_Internal_Template::$cache_id)

```php
public string $cache_id
```






***

### cache_lifetime

saved cache lifetime in seconds

```php
public int $cache_lifetime
```






***

### lock_id

Id for cache locking

```php
public string $lock_id
```






***

### is_locked

flag that cache is locked by this instance

```php
public bool $is_locked
```






***

### source

Source Object

```php
public \Smarty_Template_Source $source
```






***

### hashes

Nocache hash codes of processed compiled templates

```php
public array $hashes
```






***

### isCache

Flag if this is a cache resource

```php
public bool $isCache
```






***

## Methods


### __construct

create Cached Object container

```php
public __construct(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### load



```php
public static load(\Smarty_Internal_Template $_template): \Smarty_Template_Cached
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |





***

### render

Render cache template

```php
public render(\Smarty_Internal_Template $_template, bool $no_output_filter = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |
| `$no_output_filter` | **bool** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### isCached

Check if cache is valid, lock cache if required

```php
public isCached(\Smarty_Internal_Template $_template): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |


**Return Value:**

flag true if cache is valid




***

### process

Process cached template

```php
public process(\Smarty_Internal_Template $_template, bool $update = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |
| `$update` | **bool** | flag if called because cache update |





***

### read

Read cache content from handler

```php
public read(\Smarty_Internal_Template $_template): string|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |


**Return Value:**

content




***


## Inherited methods


### process

Process resource

```php
public process(\Smarty_Internal_Template $_template): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |





***

### getRenderedTemplateCode

get rendered template content by calling compiled or cached template code

```php
public getRenderedTemplateCode(\Smarty_Internal_Template $_template, string $unifunc = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |
| `$unifunc` | **string** | function with template code |




**Throws:**

- [`Exception`](./Exception.md)



***

### getTimeStamp

Get compiled time stamp

```php
public getTimeStamp(): int
```












***


***
> Automatically generated on 2025-03-15
