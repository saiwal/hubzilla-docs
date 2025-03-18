
# Smarty_Internal_Method_GetTemplateVars

Smarty Method GetTemplateVars

Smarty::getTemplateVars() method

* Full name: `\Smarty_Internal_Method_GetTemplateVars`



## Properties


### objMap

Valid for all objects

```php
public int $objMap
```






***

## Methods


### getTemplateVars

Returns a single or all template variables

```php
public getTemplateVars(\Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $data, string $varName = null, \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $_ptr = null, bool $searchParents = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$varName` | **string** | variable name or null |
| `$_ptr` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** | optional pointer to data object |
| `$searchParents` | **bool** | include parent templates? |


**Return Value:**

variable value or or array of variables




**See Also:**

* https://www.smarty.net/docs/en/api.get.template.vars.tpl - 

***

### _getVariable

gets the object of a Smarty variable

```php
public _getVariable(\Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $data, string $varName, \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $_ptr = null, bool $searchParents = true, bool $errorEnable = true): \Smarty_Variable
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$varName` | **string** | the name of the Smarty variable |
| `$_ptr` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** | optional pointer to data object |
| `$searchParents` | **bool** | search also in parent data |
| `$errorEnable` | **bool** |  |





***


***
> Automatically generated on 2025-03-18
