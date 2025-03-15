***

# Smarty_Internal_Runtime_UpdateCache

Inline Runtime Methods render, setSourceByUid, setupSubTemplate



* Full name: `\Smarty_Internal_Runtime_UpdateCache`




## Methods


### cacheModifiedCheck

check client side cache

```php
public cacheModifiedCheck(\Smarty_Template_Cached $cached, \Smarty_Internal_Template $_template, string $content): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cached` | **\Smarty_Template_Cached** |  |
| `$_template` | **\Smarty_Internal_Template** |  |
| `$content` | **string** |  |





***

### updateCache

Cache was invalid , so render from compiled and write to cache

```php
public updateCache(\Smarty_Template_Cached $cached, \Smarty_Internal_Template $_template, mixed $no_output_filter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cached` | **\Smarty_Template_Cached** |  |
| `$_template` | **\Smarty_Internal_Template** |  |
| `$no_output_filter` | **mixed** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### removeNoCacheHash

Sanitize content and write it to cache resource

```php
public removeNoCacheHash(\Smarty_Template_Cached $cached, \Smarty_Internal_Template $_template, bool $no_output_filter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cached` | **\Smarty_Template_Cached** |  |
| `$_template` | **\Smarty_Internal_Template** |  |
| `$no_output_filter` | **bool** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### writeCachedContent

Writes the content to cache resource

```php
public writeCachedContent(\Smarty_Internal_Template $_template, string $content): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |
| `$content` | **string** |  |





***

### write

Write this cache object to handler

```php
public write(\Smarty_Internal_Template $_template, string $content): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |
| `$content` | **string** | content to cache |


**Return Value:**

success




***


***
> Automatically generated on 2025-03-15
