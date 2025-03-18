
# Smarty_Data

class for the Smarty data object
The Smarty data object will hold Smarty variables in the current scope



* Full name: `\Smarty_Data`
* Parent class: [`\Smarty_Internal_Data`](./Smarty_Internal_Data.md)



## Properties


### count

Counter

```php
public static int $count
```



* This property is **static**.


***

### dataObjectName

Data block name

```php
public string $dataObjectName
```






***

### smarty

Smarty object

```php
public \Smarty $smarty
```






***

## Methods


### __construct

create Smarty data object

```php
public __construct(\Smarty|array $_parent = null, \Smarty|\Smarty_Internal_Template $smarty = null, string $name = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_parent` | **\Smarty&#124;array** | parent template |
| `$smarty` | **\Smarty&#124;\Smarty_Internal_Template** | global smarty instance |
| `$name` | **string** | optional data block name |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


## Inherited methods


### __construct

Smarty_Internal_Data constructor.

```php
public __construct(): mixed
```

Install extension handler










***

### assign

assigns a Smarty variable

```php
public assign(array|string $tpl_var, mixed $value = null, bool $nocache = false): \Smarty_Internal_Data
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl_var` | **array&#124;string** | the template variable name(s) |
| `$value` | **mixed** | the value to assign |
| `$nocache` | **bool** | if true any output of this variable will be not cached |


**Return Value:**

current Smarty_Internal_Data (or Smarty or Smarty_Internal_Template) instance for
chaining




***

### append

appends values to template variables

```php
public append(array|string $tpl_var, mixed $value = null, bool $merge = false, bool $nocache = false): \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl_var` | **array&#124;string** | the template variable name(s) |
| `$value` | **mixed** | the value to append |
| `$merge` | **bool** | flag if array elements shall be merged |
| `$nocache` | **bool** | if true any output of this variable will<br />be not cached |





**See Also:**

* https://www.smarty.net/docs/en/api.append.tpl - 

***

### assignGlobal

assigns a global Smarty variable

```php
public assignGlobal(string $varName, mixed $value = null, bool $nocache = false): \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$varName` | **string** | the global variable name |
| `$value` | **mixed** | the value to assign |
| `$nocache` | **bool** | if true any output of this variable will be not cached |





***

### appendByRef

appends values to template variables by reference

```php
public appendByRef(string $tpl_var, mixed& $value, bool $merge = false): \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl_var` | **string** | the template variable name |
| `$value` | **mixed** | the referenced value to append |
| `$merge` | **bool** | flag if array elements shall be merged |





***

### assignByRef

assigns values to template variables by reference

```php
public assignByRef(string $tpl_var, mixed& $value, bool $nocache = false): \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl_var` | **string** | the template variable name |
| `$value` | **mixed** |  |
| `$nocache` | **bool** | if true any output of this variable will be not cached |





***

### getTemplateVars

Returns a single or all template variables

```php
public getTemplateVars(string $varName = null, \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $_ptr = null, bool $searchParents = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$varName` | **string** | variable name or null |
| `$_ptr` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** | optional pointer to data object |
| `$searchParents` | **bool** | include parent templates? |


**Return Value:**

variable value or or array of variables




**See Also:**

* https://www.smarty.net/docs/en/api.get.template.vars.tpl - 

***

### _mergeVars

Follow the parent chain an merge template and config variables

```php
public _mergeVars(\Smarty_Internal_Data|null $data = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;null** |  |





***

### _isDataObj

Return true if this instance is a Data obj

```php
public _isDataObj(): bool
```












***

### _isTplObj

Return true if this instance is a template obj

```php
public _isTplObj(): bool
```












***

### _isSmartyObj

Return true if this instance is a Smarty obj

```php
public _isSmartyObj(): bool
```












***

### _getSmartyObj

Get Smarty object

```php
public _getSmartyObj(): \Smarty
```












***

### __call

Handle unknown class methods

```php
public __call(string $name, array $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | unknown method-name |
| `$args` | **array** | argument array |





***


***
> Automatically generated on 2025-03-18
