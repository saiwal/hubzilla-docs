
# Smarty_Internal_Method_ClearAllCache

Smarty Method ClearAllCache

Smarty::clearAllCache() method

* Full name: `\Smarty_Internal_Method_ClearAllCache`



## Properties


### objMap

Valid for Smarty object

```php
public int $objMap
```






***

## Methods


### clearAllCache

Empty cache folder

```php
public clearAllCache(\Smarty $smarty, int $exp_time = null, string $type = null): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$exp_time` | **int** | expiration time |
| `$type` | **string** | resource type |


**Return Value:**

number of cache files deleted



**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.clear.all.cache.tpl - 

***


***
> Automatically generated on 2025-03-15
