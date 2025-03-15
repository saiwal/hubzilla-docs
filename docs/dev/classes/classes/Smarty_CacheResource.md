***

# Smarty_CacheResource

Cache Handler API



* Full name: `\Smarty_CacheResource`
* This class is an **Abstract class**



## Properties


### sysplugins

resource types provided by the core

```php
protected static array $sysplugins
```



* This property is **static**.


***

## Methods


### populate

populate Cached Object with meta data from Resource

```php
public populate(\Smarty_Template_Cached $cached, \Smarty_Internal_Template $_template): void
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cached` | **\Smarty_Template_Cached** | cached object |
| `$_template` | **\Smarty_Internal_Template** | template object |





***

### populateTimestamp

populate Cached Object with timestamp and exists from Resource

```php
public populateTimestamp(\Smarty_Template_Cached $cached): void
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cached` | **\Smarty_Template_Cached** |  |





***

### process

Read the cached template and process header

```php
public process(\Smarty_Internal_Template $_template, \Smarty_Template_Cached $cached = null, bool $update = false): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |
| `$cached` | **\Smarty_Template_Cached** | cached object |
| `$update` | **bool** | flag if called because cache update |


**Return Value:**

true or false if the cached content does not exist




***

### writeCachedContent

Write the rendered template output to cache

```php
public writeCachedContent(\Smarty_Internal_Template $_template, string $content): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |
| `$content` | **string** | content to cache |


**Return Value:**

success




***

### readCachedContent

Read cached template from cache

```php
public readCachedContent(\Smarty_Internal_Template $_template): string
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |


**Return Value:**

content




***

### getCachedContent

Return cached content

```php
public getCachedContent(\Smarty_Internal_Template $_template): null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |





***

### clearAll

Empty cache

```php
public clearAll(\Smarty $smarty, int $exp_time = null): int
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty object |
| `$exp_time` | **int** | expiration time (number of seconds, not timestamp) |


**Return Value:**

number of cache files deleted




***

### clear

Empty cache for a specific template

```php
public clear(\Smarty $smarty, string $resource_name, string $cache_id, string $compile_id, int $exp_time): int
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty object |
| `$resource_name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$exp_time` | **int** | expiration time (number of seconds, not timestamp) |


**Return Value:**

number of cache files deleted




***

### locked



```php
public locked(\Smarty $smarty, \Smarty_Template_Cached $cached): bool|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$cached` | **\Smarty_Template_Cached** |  |





***

### hasLock

Check is cache is locked for this template

```php
public hasLock(\Smarty $smarty, \Smarty_Template_Cached $cached): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$cached` | **\Smarty_Template_Cached** |  |





***

### acquireLock

Lock cache for this template

```php
public acquireLock(\Smarty $smarty, \Smarty_Template_Cached $cached): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$cached` | **\Smarty_Template_Cached** |  |





***

### releaseLock

Unlock cache for this template

```php
public releaseLock(\Smarty $smarty, \Smarty_Template_Cached $cached): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$cached` | **\Smarty_Template_Cached** |  |





***

### load

Load Cache Resource Handler

```php
public static load(\Smarty $smarty, string $type = null): \Smarty_CacheResource
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty object |
| `$type` | **string** | name of the cache resource |


**Return Value:**

Cache Resource Handler



**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
