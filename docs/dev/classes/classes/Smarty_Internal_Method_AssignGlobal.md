
# Smarty_Internal_Method_AssignGlobal

Smarty Method AssignGlobal

Smarty::assignGlobal() method

* Full name: `\Smarty_Internal_Method_AssignGlobal`



## Properties


### objMap

Valid for all objects

```php
public int $objMap
```






***

## Methods


### assignGlobal

assigns a global Smarty variable

```php
public assignGlobal(\Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $data, string $varName, mixed $value = null, bool $nocache = false): \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$varName` | **string** | the global variable name |
| `$value` | **mixed** | the value to assign |
| `$nocache` | **bool** | if true any output of this variable will<br />be not cached |





***


***
> Automatically generated on 2025-03-15
