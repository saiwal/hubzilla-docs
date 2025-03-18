
# Smarty_Internal_Method_GetConfigVars

Smarty Method GetConfigVars

Smarty::getConfigVars() method

* Full name: `\Smarty_Internal_Method_GetConfigVars`



## Properties


### objMap

Valid for all objects

```php
public int $objMap
```






***

## Methods


### getConfigVars

Returns a single or all config variables

```php
public getConfigVars(\Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $data, string $varname = null, bool $search_parents = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$varname` | **string** | variable name or null |
| `$search_parents` | **bool** | include parent templates? |


**Return Value:**

variable value or or array of variables




**See Also:**

* https://www.smarty.net/docs/en/api.get.config.vars.tpl - 

***


***
> Automatically generated on 2025-03-18
