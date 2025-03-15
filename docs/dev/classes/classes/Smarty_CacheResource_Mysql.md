***

# Smarty_CacheResource_Mysql

MySQL CacheResource
CacheResource Implementation based on the Custom API to use
MySQL as the storage resource for Smarty's output caching.

Table definition:
<pre>CREATE TABLE IF NOT EXISTS `output_cache` (
  `id` CHAR(40) NOT NULL COMMENT 'sha1 hash',
  `name` VARCHAR(250) NOT NULL,
  `cache_id` VARCHAR(250) NULL DEFAULT NULL,
  `compile_id` VARCHAR(250) NULL DEFAULT NULL,
  `modified` TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `content` LONGTEXT NOT NULL,
  PRIMARY KEY (`id`),
  INDEX(`name`),
  INDEX(`cache_id`),
  INDEX(`compile_id`),
  INDEX(`modified`)
) ENGINE = InnoDB;</pre>

* Full name: `\Smarty_CacheResource_Mysql`
* Parent class: [`\Smarty_CacheResource_Custom`](./Smarty_CacheResource_Custom.md)



## Properties


### db



```php
protected \PDO $db
```






***

### fetch



```php
protected \PDOStatement $fetch
```






***

### fetchTimestamp



```php
protected \PDOStatement $fetchTimestamp
```






***

### save



```php
protected \PDOStatement $save
```






***

## Methods


### __construct

Smarty_CacheResource_Mysql constructor.

```php
public __construct(): mixed
```











**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### fetch

fetch cached content and its modification time from data source

```php
protected fetch(string $id, string $name, string $cache_id, string $compile_id, string& $content, int& $mtime): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | unique cache content identifier |
| `$name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$content` | **string** | cached content |
| `$mtime` | **int** | cache modification timestamp (epoch) |





***

### fetchTimestamp

Fetch cached content's modification timestamp from data source

```php
protected fetchTimestamp(string $id, string $name, string $cache_id, string $compile_id): int|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | unique cache content identifier |
| `$name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |


**Return Value:**

timestamp (epoch) the template was modified, or false if not found




***

### save

Save content to cache

```php
protected save(string $id, string $name, string $cache_id, string $compile_id, int|null $exp_time, string $content): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | unique cache content identifier |
| `$name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$exp_time` | **int&#124;null** | seconds till expiration time in seconds or null |
| `$content` | **string** | content to cache |


**Return Value:**

success




***

### delete

Delete content from cache

```php
protected delete(string $name, string $cache_id, string $compile_id, int|null $exp_time): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$exp_time` | **int&#124;null** | seconds till expiration or null |


**Return Value:**

number of deleted caches




***


## Inherited methods


### populate

populate Cached Object with meta data from Resource

```php
public populate(\Smarty_Template_Cached $cached, \Smarty_Internal_Template $_template): void
```








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








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cached` | **\Smarty_Template_Cached** |  |





***

### process

Read the cached template and process the header

```php
public process(\Smarty_Internal_Template $_smarty_tpl, \Smarty_Template_Cached $cached = null, bool $update = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_smarty_tpl` | **\Smarty_Internal_Template** | do not change variable name, is used by compiled template |
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
public readCachedContent(\Smarty_Internal_Template $_template): string|bool
```








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



**Throws:**

- [`SmartyException`](./SmartyException.md)



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
| `$smarty` | **\Smarty** | Smarty object |
| `$cached` | **\Smarty_Template_Cached** | cached object |


**Return Value:**

true or false if cache is locked




***

### acquireLock

Lock cache for this template

```php
public acquireLock(\Smarty $smarty, \Smarty_Template_Cached $cached): bool|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty object |
| `$cached` | **\Smarty_Template_Cached** | cached object |





***

### releaseLock

Unlock cache for this template

```php
public releaseLock(\Smarty $smarty, \Smarty_Template_Cached $cached): bool|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty object |
| `$cached` | **\Smarty_Template_Cached** | cached object |





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

### fetch

fetch cached content and its modification time from data source

```php
protected fetch(string $id, string $name, string $cache_id, string $compile_id, string& $content, int& $mtime): void
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | unique cache content identifier |
| `$name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$content` | **string** | cached content |
| `$mtime` | **int** | cache modification timestamp (epoch) |





***

### fetchTimestamp

Fetch cached content's modification timestamp from data source
{@internal implementing this method is optional.

```php
protected fetchTimestamp(string $id, string $name, string $cache_id, string $compile_id): int|bool
```

Only implement it if modification times can be accessed faster than loading the complete cached content.}}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | unique cache content identifier |
| `$name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |


**Return Value:**

timestamp (epoch) the template was modified, or false if not found




***

### save

Save content to cache

```php
protected save(string $id, string $name, string $cache_id, string $compile_id, int|null $exp_time, string $content): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | unique cache content identifier |
| `$name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$exp_time` | **int&#124;null** | seconds till expiration or null |
| `$content` | **string** | content to cache |


**Return Value:**

success




***

### delete

Delete content from cache

```php
protected delete(string|null $name, string|null $cache_id, string|null $compile_id, int|null $exp_time): int
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string&#124;null** | template name |
| `$cache_id` | **string&#124;null** | cache id |
| `$compile_id` | **string&#124;null** | compile id |
| `$exp_time` | **int&#124;null** | seconds till expiration time in seconds or null |


**Return Value:**

number of deleted caches




***


***
> Automatically generated on 2025-03-15
