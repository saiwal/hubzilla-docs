
# Smarty_Internal_Runtime_CacheResourceFile

Smarty Internal Runtime Cache Resource File Class



* Full name: `\Smarty_Internal_Runtime_CacheResourceFile`




## Methods


### clear

Empty cache for a specific template

```php
public clear(\Smarty $smarty, string $resource_name, string $cache_id, string $compile_id, int $exp_time): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$resource_name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$exp_time` | **int** | expiration time (number of seconds, not timestamp) |


**Return Value:**

number of cache files deleted




***


***
> Automatically generated on 2025-03-15
