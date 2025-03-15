
# Smarty_Internal_Template

Main class with template data structures and methods



* Full name: `\Smarty_Internal_Template`
* Parent class: [`\Smarty_Internal_TemplateBase`](./Smarty_Internal_TemplateBase.md)



## Properties


### tplObjCache

Template object cache

```php
public static \Smarty_Internal_Template[] $tplObjCache
```



* This property is **static**.


***

### isCacheTplObj

Template object cache for Smarty::isCached() === true

```php
public static \Smarty_Internal_Template[] $isCacheTplObj
```



* This property is **static**.


***

### subTplInfo

Sub template Info Cache
- index name
- value use count

```php
public static int[] $subTplInfo
```



* This property is **static**.


***

### _objType

This object type (Smarty = 1, template = 2, data = 4)

```php
public int $_objType
```






***

### smarty

Global smarty instance

```php
public \Smarty $smarty
```






***

### source

Source instance

```php
public \Smarty_Template_Source|\Smarty_Template_Config $source
```






***

### inheritance

Inheritance runtime extension

```php
public \Smarty_Internal_Runtime_Inheritance $inheritance
```






***

### template_resource

Template resource

```php
public string $template_resource
```






***

### mustCompile

flag if compiled template is invalid and must be (re)compiled

```php
public bool $mustCompile
```






***

### templateId

Template Id

```php
public null|string $templateId
```






***

### scope

Scope in which variables shall be assigned

```php
public int $scope
```






***

### isRenderingCache

Flag which is set while rending a cache file

```php
public bool $isRenderingCache
```






***

### startRenderCallbacks

Callbacks called before rendering template

```php
public callable[] $startRenderCallbacks
```






***

### endRenderCallbacks

Callbacks called after rendering template

```php
public callable[] $endRenderCallbacks
```






***

## Methods


### __construct

Create template data object
Some of the global Smarty settings copied to template scope
It load the required template resources and caching plugins

```php
public __construct(string $template_resource, \Smarty $smarty, null|\Smarty_Internal_Template|\Smarty|\Smarty_Internal_Data $_parent = null, mixed $_cache_id = null, mixed $_compile_id = null, bool|int|null $_caching = null, int|null $_cache_lifetime = null, bool $_isConfig = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template_resource` | **string** | template resource string |
| `$smarty` | **\Smarty** | Smarty instance |
| `$_parent` | **null&#124;\Smarty_Internal_Template&#124;\Smarty&#124;\Smarty_Internal_Data** | back pointer to parent<br />object with variables or<br />null |
| `$_cache_id` | **mixed** | cache   id or null |
| `$_compile_id` | **mixed** | compile id or null |
| `$_caching` | **bool&#124;int&#124;null** | use caching? |
| `$_cache_lifetime` | **int&#124;null** | cache life-time in<br />seconds |
| `$_isConfig` | **bool** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### render

render template

```php
public render(bool $no_output_filter = true, null|bool $display = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$no_output_filter` | **bool** | if true do not run output filter |
| `$display` | **null&#124;bool** | true: display, false: fetch null: sub-template |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



***

### _subTemplateRender

Runtime function to render sub-template

```php
public _subTemplateRender(string $template, mixed $cache_id, mixed $compile_id, int $caching, int $cache_lifetime, array $data, int $scope, bool $forceTplCache, string $uid = null, string $content_func = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **string** | template name |
| `$cache_id` | **mixed** | cache id |
| `$compile_id` | **mixed** | compile id |
| `$caching` | **int** | cache mode |
| `$cache_lifetime` | **int** | life time of cache data |
| `$data` | **array** | passed parameter template variables |
| `$scope` | **int** | scope in which {include} should execute |
| `$forceTplCache` | **bool** | cache template object |
| `$uid` | **string** | file dependency uid |
| `$content_func` | **string** | function name |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



***

### _subTemplateRegister

Get called sub-templates and save call count

```php
public _subTemplateRegister(): mixed
```












***

### _isSubTpl

Check if this is a sub template

```php
public _isSubTpl(): bool
```









**Return Value:**

true is sub template




***

### _assignInScope

Assign variable in scope

```php
public _assignInScope(string $varName, mixed $value, bool $nocache = false, int $scope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$varName` | **string** | variable name |
| `$value` | **mixed** | value |
| `$nocache` | **bool** | nocache flag |
| `$scope` | **int** | scope into which variable shall be assigned |





***

### _checkPlugins

Check if plugins are callable require file otherwise

```php
public _checkPlugins(array $plugins): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plugins` | **array** | required plugins |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### _decodeProperties

This function is executed automatically when a compiled or cached template file is included
- Decode saved properties from compiled template and cache files
- Check if compiled or cache file is valid

```php
public _decodeProperties(\Smarty_Internal_Template $tpl, array $properties, bool $cache = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$properties` | **array** | special template properties |
| `$cache` | **bool** | flag if called from cache file |


**Return Value:**

flag if compiled or cache file is valid



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### compileTemplateSource

Compiles the template
If the template is not evaluated the compiled template is saved on disk

```php
public compileTemplateSource(): mixed
```











**Throws:**

- [`Exception`](./Exception.md)



***

### writeCachedContent

Writes the content to cache resource

```php
public writeCachedContent(string $content): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **string** |  |





***

### _getTemplateId

Get unique template id

```php
public _getTemplateId(): string
```











**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### capture_error

runtime error not matching capture tags

```php
public capture_error(): mixed
```











**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### loadCompiled

Load compiled object

```php
public loadCompiled(bool $force = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$force` | **bool** | force new compiled object |





***

### loadCached

Load cached object

```php
public loadCached(bool $force = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$force` | **bool** | force new cached object |





***

### _loadInheritance

Load inheritance object

```php
public _loadInheritance(): mixed
```












***

### _cleanUp

Unload inheritance object

```php
public _cleanUp(): mixed
```












***

### loadCompiler

Load compiler object

```php
public loadCompiler(): mixed
```











**Throws:**

- [`SmartyException`](./SmartyException.md)



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

### __get

get Smarty property in template context

```php
public __get(string $property_name): mixed|\Smarty_Template_Cached
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property_name` | **string** | property name |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### __set

set Smarty property in template context

```php
public __set(string $property_name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property_name` | **string** | property name |
| `$value` | **mixed** | value |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### __destruct

Template data object destructor

```php
public __destruct(): mixed
```












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


***
> Automatically generated on 2025-03-15
