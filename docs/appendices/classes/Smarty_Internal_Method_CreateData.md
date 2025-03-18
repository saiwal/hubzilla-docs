
# Smarty_Internal_Method_CreateData

Smarty Method CreateData

Smarty::createData() method

* Full name: `\Smarty_Internal_Method_CreateData`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### createData

creates a data object

```php
public createData(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, \Smarty_Internal_Template|\Smarty_Internal_Data|\Smarty_Data|\Smarty $parent = null, string $name = null): \Smarty_Data
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$parent` | **\Smarty_Internal_Template&#124;\Smarty_Internal_Data&#124;\Smarty_Data&#124;\Smarty** | next higher level of Smarty<br />variables |
| `$name` | **string** | optional data block name |


**Return Value:**

data object




**See Also:**

* https://www.smarty.net/docs/en/api.create.data.tpl - 

***


***
> Automatically generated on 2025-03-18
