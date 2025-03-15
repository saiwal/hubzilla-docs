
# Smarty_CacheResource_Apc

APC CacheResource
CacheResource Implementation based on the KeyValueStore API to use
memcache as the storage resource for Smarty's output caching.

*

* Full name: `\Smarty_CacheResource_Apc`
* Parent class: [`\Smarty_CacheResource_KeyValueStore`](./Smarty_CacheResource_KeyValueStore.md)




## Methods


### __construct

Smarty_CacheResource_Apc constructor.

```php
public __construct(): mixed
```











**Throws:**

- [`Exception`](./Exception.md)



***

### read

Read values for a set of keys from cache

```php
protected read(array $keys): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keys` | **array** | list of keys to fetch |


**Return Value:**

list of values with the given keys used as indexes




***

### write

Save values for a set of keys to cache

```php
protected write(array $keys, int $expire = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keys` | **array** | list of values to save |
| `$expire` | **int** | expiration time |


**Return Value:**

true on success, false on failure




***

### delete

Remove values from cache

```php
protected delete(array $keys): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keys` | **array** | list of keys to delete |


**Return Value:**

true on success, false on failure




***

### purge

Remove *all* values from cache

```php
protected purge(): bool
```









**Return Value:**

true on success, false on failure




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
| `$cached` | **\Smarty_Template_Cached** | cached object |





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
public readCachedContent(\Smarty_Internal_Template $_template): string|false
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
{@internal the $exp_time argument is ignored altogether }}

```php
public clearAll(\Smarty $smarty, int $exp_time = null): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty object |
| `$exp_time` | **int** | expiration time [being ignored] |


**Return Value:**

number of cache files deleted [always -1]




***

### clear

Empty cache for a specific template
{@internal the $exp_time argument is ignored altogether}}

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
| `$exp_time` | **int** | expiration time [being ignored] |


**Return Value:**

number of cache files deleted [always -1]



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

### getTemplateUid

Get template's unique ID

```php
protected getTemplateUid(\Smarty $smarty, string $resource_name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty object |
| `$resource_name` | **string** | template name |


**Return Value:**

filepath of cache file



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### sanitize

Sanitize CacheID components

```php
protected sanitize(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | CacheID component to sanitize |


**Return Value:**

sanitized CacheID component




***

### fetch

Fetch and prepare a cache object.

```php
protected fetch(string $cid, string $resource_name = null, string $cache_id = null, string $compile_id = null, string& $content = null, int& $timestamp = null, string $resource_uid = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cid` | **string** | CacheID to fetch |
| `$resource_name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$content` | **string** | cached content |
| `$timestamp` | **int** | cached timestamp (epoch) |
| `$resource_uid` | **string** | resource&#039;s uid |


**Return Value:**

success




***

### addMetaTimestamp

Add current microtime to the beginning of $cache_content
{@internal the header uses 8 Bytes, the first 4 Bytes are the seconds, the second 4 Bytes are the microseconds}}

```php
protected addMetaTimestamp(string& $content): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **string** | the content to be cached |





***

### getMetaTimestamp

Extract the timestamp the $content was cached

```php
protected getMetaTimestamp(string& $content): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **string** | the cached content |


**Return Value:**

the microtime the content was cached




***

### invalidate

Invalidate CacheID

```php
protected invalidate(string $cid = null, string $resource_name = null, string $cache_id = null, string $compile_id = null, string $resource_uid = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cid` | **string** | CacheID |
| `$resource_name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$resource_uid` | **string** | source&#039;s uid |





***

### getLatestInvalidationTimestamp

Determine the latest timestamp known to the invalidation chain

```php
protected getLatestInvalidationTimestamp(string $cid, string $resource_name = null, string $cache_id = null, string $compile_id = null, string $resource_uid = null): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cid` | **string** | CacheID to determine latest invalidation timestamp of |
| `$resource_name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$resource_uid` | **string** | source&#039;s filepath |


**Return Value:**

the microtime the CacheID was invalidated




***

### listInvalidationKeys

Translate a CacheID into the list of applicable InvalidationKeys.

```php
protected listInvalidationKeys(string $cid, string $resource_name = null, string $cache_id = null, string $compile_id = null, string $resource_uid = null): array
```

Splits 'some|chain|into|an|array' into array( '#clearAll#', 'some', 'some|chain', 'some|chain|into', ... )






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cid` | **string** | CacheID to translate |
| `$resource_name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$resource_uid` | **string** | source&#039;s filepath |


**Return Value:**

list of InvalidationKeys




***

### read

Read values for a set of keys from cache

```php
protected read(array $keys): array
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keys` | **array** | list of keys to fetch |


**Return Value:**

list of values with the given keys used as indexes




***

### write

Save values for a set of keys to cache

```php
protected write(array $keys, int $expire = null): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keys` | **array** | list of values to save |
| `$expire` | **int** | expiration time |


**Return Value:**

true on success, false on failure




***

### delete

Remove values from cache

```php
protected delete(array $keys): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keys` | **array** | list of keys to delete |


**Return Value:**

true on success, false on failure




***

### purge

Remove *all* values from cache

```php
protected purge(): bool
```









**Return Value:**

true on success, false on failure




***


***
> Automatically generated on 2025-03-15
