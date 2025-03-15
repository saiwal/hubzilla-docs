***

# Smarty_Template_Resource_Base

Smarty Template Resource Base Object



* Full name: `\Smarty_Template_Resource_Base`
* This class is an **Abstract class**



## Properties


### filepath

Compiled Filepath

```php
public string $filepath
```






***

### timestamp

Compiled Timestamp

```php
public int|bool $timestamp
```






***

### exists

Compiled Existence

```php
public bool $exists
```






***

### compile_id

Template Compile Id (Smarty_Internal_Template::$compile_id)

```php
public string $compile_id
```






***

### processed

Compiled Content Loaded

```php
public bool $processed
```






***

### unifunc

unique function name for compiled template code

```php
public string $unifunc
```






***

### has_nocache_code

flag if template does contain nocache code sections

```php
public bool $has_nocache_code
```






***

### file_dependency

resource file dependency

```php
public array $file_dependency
```






***

### content

Content buffer

```php
public string $content
```






***

### includes

Included sub templates
- index name
- value use count

```php
public int[] $includes
```






***

### isCache

Flag if this is a cache resource

```php
public bool $isCache
```






***

## Methods


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
