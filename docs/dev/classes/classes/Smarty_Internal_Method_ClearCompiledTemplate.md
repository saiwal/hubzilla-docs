
# Smarty_Internal_Method_ClearCompiledTemplate

Smarty Method ClearCompiledTemplate

Smarty::clearCompiledTemplate() method

* Full name: `\Smarty_Internal_Method_ClearCompiledTemplate`



## Properties


### objMap

Valid for Smarty object

```php
public int $objMap
```






***

## Methods


### clearCompiledTemplate

Delete compiled template file

```php
public clearCompiledTemplate(\Smarty $smarty, string $resource_name = null, string $compile_id = null, int $exp_time = null): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$resource_name` | **string** | template name |
| `$compile_id` | **string** | compile id |
| `$exp_time` | **int** | expiration time |


**Return Value:**

number of template files deleted



**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.clear.compiled.template.tpl - 

***


***
> Automatically generated on 2025-03-15
