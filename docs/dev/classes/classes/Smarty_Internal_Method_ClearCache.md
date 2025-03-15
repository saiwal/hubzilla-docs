***

# Smarty_Internal_Method_ClearCache

Smarty Method ClearCache

Smarty::clearCache() method

* Full name: `\Smarty_Internal_Method_ClearCache`



## Properties


### objMap

Valid for Smarty object

```php
public int $objMap
```






***

## Methods


### clearCache

Empty cache for a specific template

```php
public clearCache(\Smarty $smarty, string $template_name, string $cache_id = null, string $compile_id = null, int $exp_time = null, string $type = null): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$template_name` | **string** | template name |
| `$cache_id` | **string** | cache id |
| `$compile_id` | **string** | compile id |
| `$exp_time` | **int** | expiration time |
| `$type` | **string** | resource type |


**Return Value:**

number of cache files deleted



**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.clear.cache.tpl - 

***


***
> Automatically generated on 2025-03-15
