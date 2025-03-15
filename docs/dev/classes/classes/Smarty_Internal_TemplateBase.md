
# Smarty_Internal_TemplateBase

Class with shared smarty/template methods



* Full name: `\Smarty_Internal_TemplateBase`
* Parent class: [`\Smarty_Internal_Data`](./Smarty_Internal_Data.md)
* This class is an **Abstract class**



## Properties


### cache_id

Set this if you want different sets of cache files for the same
templates.

```php
public string $cache_id
```






***

### compile_id

Set this if you want different sets of compiled files for the same
templates.

```php
public string $compile_id
```






***

### caching

caching enabled

```php
public int $caching
```






***

### compile_check

check template for modifications?

```php
public int $compile_check
```






***

### cache_lifetime

cache lifetime in seconds

```php
public int $cache_lifetime
```






***

### tplFunctions

Array of source information for known template functions

```php
public array $tplFunctions
```






***

### _cache

universal cache

```php
public $_cache
```






***

## Methods


### fetch

fetches a rendered Smarty template

```php
public fetch(string $template = null, mixed $cache_id = null, mixed $compile_id = null, object $parent = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **string** | the resource handle of the template file or template object |
| `$cache_id` | **mixed** | cache id to be used with this template |
| `$compile_id` | **mixed** | compile id to be used with this template |
| `$parent` | **object** | next higher level of Smarty variables |


**Return Value:**

rendered template output



**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



***

### display

displays a Smarty template

```php
public display(string $template = null, mixed $cache_id = null, mixed $compile_id = null, object $parent = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **string** | the resource handle of the template file or template object |
| `$cache_id` | **mixed** | cache id to be used with this template |
| `$compile_id` | **mixed** | compile id to be used with this template |
| `$parent` | **object** | next higher level of Smarty variables |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



***

### isCached

test if cache is valid

```php
public isCached(null|string|\Smarty_Internal_Template $template = null, mixed $cache_id = null, mixed $compile_id = null, object $parent = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **null&#124;string&#124;\Smarty_Internal_Template** | the resource handle of the template file or template<br />object |
| `$cache_id` | **mixed** | cache id to be used with this template |
| `$compile_id` | **mixed** | compile id to be used with this template |
| `$parent` | **object** | next higher level of Smarty variables |


**Return Value:**

cache status



**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.is.cached.tpl - 

***

### _execute

fetches a rendered Smarty template

```php
private _execute(string $template, mixed $cache_id, mixed $compile_id, object $parent, string $function): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **string** | the resource handle of the template file or template object |
| `$cache_id` | **mixed** | cache id to be used with this template |
| `$compile_id` | **mixed** | compile id to be used with this template |
| `$parent` | **object** | next higher level of Smarty variables |
| `$function` | **string** | function type 0 = fetch,  1 = display, 2 = isCache |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



***

### registerPlugin

Registers plugin to be used in templates

```php
public registerPlugin(string $type, string $name, callable $callback, bool $cacheable = true, mixed $cache_attr = null): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | plugin type |
| `$name` | **string** | name of template tag |
| `$callback` | **callable** | PHP callback to register |
| `$cacheable` | **bool** | if true (default) this function is cache able |
| `$cache_attr` | **mixed** | caching attributes if any |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.plugin.tpl - 

***

### loadFilter

load a filter of specified type and name

```php
public loadFilter(string $type, string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | filter type |
| `$name` | **string** | filter name |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.load.filter.tpl - 

***

### registerFilter

Registers a filter function

```php
public registerFilter(string $type, callable $callback, string|null $name = null): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | filter type |
| `$callback` | **callable** |  |
| `$name` | **string&#124;null** | optional filter name |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.filter.tpl - 

***

### registerObject

Registers object to be used in templates

```php
public registerObject(string $object_name, object $object, array $allowed_methods_properties = array(), bool $format = true, array $block_methods = array()): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$object_name` | **string** |  |
| `$object` | **object** | the referenced PHP object to register |
| `$allowed_methods_properties` | **array** | list of allowed methods (empty = all) |
| `$format` | **bool** | smarty argument format, else traditional |
| `$block_methods` | **array** | list of block-methods |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.object.tpl - 

***

### setCompileCheck



```php
public setCompileCheck(int $compile_check): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compile_check` | **int** |  |





***

### setCaching



```php
public setCaching(int $caching): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caching` | **int** |  |





***

### setCacheLifetime



```php
public setCacheLifetime(int $cache_lifetime): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cache_lifetime` | **int** |  |





***

### setCompileId



```php
public setCompileId(string $compile_id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compile_id` | **string** |  |





***

### setCacheId



```php
public setCacheId(string $cache_id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cache_id` | **string** |  |





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
