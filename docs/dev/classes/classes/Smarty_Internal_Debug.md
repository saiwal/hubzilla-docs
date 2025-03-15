
# Smarty_Internal_Debug

Smarty Internal Plugin Debug Class



* Full name: `\Smarty_Internal_Debug`
* Parent class: [`\Smarty_Internal_Data`](./Smarty_Internal_Data.md)



## Properties


### template_data

template data

```php
public array $template_data
```






***

### ignore_uid

List of uid's which shall be ignored

```php
public array $ignore_uid
```






***

### index

Index of display() and fetch() calls

```php
public int $index
```






***

### offset

Counter for window offset

```php
public int $offset
```






***

## Methods


### start_template

Start logging template

```php
public start_template(\Smarty_Internal_Template $template, null $mode = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** | template |
| `$mode` | **null** | true: display   false: fetch  null: subtemplate |





***

### end_template

End logging of cache time

```php
public end_template(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** | cached template |





***

### start_compile

Start logging of compile time

```php
public start_compile(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |





***

### end_compile

End logging of compile time

```php
public end_compile(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |





***

### start_render

Start logging of render time

```php
public start_render(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |





***

### end_render

End logging of compile time

```php
public end_render(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |





***

### start_cache

Start logging of cache time

```php
public start_cache(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** | cached template |





***

### end_cache

End logging of cache time

```php
public end_cache(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** | cached template |





***

### register_template

Register template object

```php
public register_template(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** | cached template |





***

### register_data

Register data object

```php
public static register_data(\Smarty_Data $data): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Data** | data object |





***

### display_debug

Opens a window for the Smarty Debugging Console and display the data

```php
public display_debug(\Smarty_Internal_Template|\Smarty $obj, bool $full = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_Template&#124;\Smarty** | object to debug |
| `$full` | **bool** |  |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



***

### get_debug_vars

Recursively gets variables from all template/data scopes

```php
public get_debug_vars(\Smarty_Internal_Template|\Smarty_Data $obj): \StdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_Template&#124;\Smarty_Data** | object to debug |





***

### get_key

Return key into $template_data for template

```php
private get_key(\Smarty_Internal_Template $template): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** | template object |


**Return Value:**

key into $template_data




***

### ignore

Ignore template

```php
public ignore(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |





***

### debugUrl

handle 'URL' debugging mode

```php
public debugUrl(\Smarty $smarty): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |





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
> Automatically generated on 2025-03-15
