***

# Smarty_Internal_Method_Append

Smarty Method Append

Smarty::append() method

* Full name: `\Smarty_Internal_Method_Append`



## Properties


### objMap

Valid for all objects

```php
public int $objMap
```






***

## Methods


### append

appends values to template variables

```php
public append(\Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $data, array|string $tpl_var, mixed $value = null, bool $merge = false, bool $nocache = false): \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$tpl_var` | **array&#124;string** | the template variable name(s) |
| `$value` | **mixed** | the value to append |
| `$merge` | **bool** | flag if array elements shall be merged |
| `$nocache` | **bool** | if true any output of this variable will<br />be not cached |





**See Also:**

* https://www.smarty.net/docs/en/api.append.tpl - 

***


***
> Automatically generated on 2025-03-15
