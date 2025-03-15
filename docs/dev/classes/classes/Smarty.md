
# Smarty

This is the main Smarty class



* Full name: `\Smarty`
* Parent class: [`\Smarty_Internal_TemplateBase`](./Smarty_Internal_TemplateBase.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`SMARTY_VERSION`|public| |&#039;4.5.4&#039;|
|`SCOPE_LOCAL`|public| |1|
|`SCOPE_PARENT`|public| |2|
|`SCOPE_TPL_ROOT`|public| |4|
|`SCOPE_ROOT`|public| |8|
|`SCOPE_SMARTY`|public| |16|
|`SCOPE_GLOBAL`|public| |32|
|`CACHING_OFF`|public| |0|
|`CACHING_LIFETIME_CURRENT`|public| |1|
|`CACHING_LIFETIME_SAVED`|public| |2|
|`CLEAR_EXPIRED`|public| |-1|
|`COMPILECHECK_OFF`|public| |0|
|`COMPILECHECK_ON`|public| |1|
|`COMPILECHECK_CACHEMISS`|public| |2|
|`DEBUG_OFF`|public| |0|
|`DEBUG_ON`|public| |1|
|`DEBUG_INDIVIDUAL`|public| |2|
|`FILTER_POST`|public| |&#039;post&#039;|
|`FILTER_PRE`|public| |&#039;pre&#039;|
|`FILTER_OUTPUT`|public| |&#039;output&#039;|
|`FILTER_VARIABLE`|public| |&#039;variable&#039;|
|`PLUGIN_FUNCTION`|public| |&#039;function&#039;|
|`PLUGIN_BLOCK`|public| |&#039;block&#039;|
|`PLUGIN_COMPILER`|public| |&#039;compiler&#039;|
|`PLUGIN_MODIFIER`|public| |&#039;modifier&#039;|
|`PLUGIN_MODIFIERCOMPILER`|public| |&#039;modifiercompiler&#039;|

## Properties


### global_tpl_vars

assigned global tpl vars

```php
public static $global_tpl_vars
```



* This property is **static**.


***

### _MBSTRING

Flag denoting if Multibyte String functions are available

```php
public static $_MBSTRING
```



* This property is **static**.


***

### _CHARSET

The character set to adhere to (e.g. "UTF-8")

```php
public static $_CHARSET
```



* This property is **static**.


***

### _DATE_FORMAT

The date format to be used internally
(accepts date() and strftime())

```php
public static $_DATE_FORMAT
```



* This property is **static**.


***

### _UTF8_MODIFIER

Flag denoting if PCRE should run in UTF-8 mode

```php
public static $_UTF8_MODIFIER
```



* This property is **static**.


***

### _IS_WINDOWS

Flag denoting if operating system is windows

```php
public static $_IS_WINDOWS
```



* This property is **static**.


***

### auto_literal

auto literal on delimiters with whitespace

```php
public bool $auto_literal
```






***

### error_unassigned

display error on not assigned variables

```php
public bool $error_unassigned
```






***

### use_include_path

look up relative file path in include_path

```php
public bool $use_include_path
```






***

### _templateDirNormalized

flag if template_dir is normalized

```php
public bool $_templateDirNormalized
```






***

### _joined_template_dir

joined template directory string used in cache keys

```php
public string $_joined_template_dir
```






***

### _configDirNormalized

flag if config_dir is normalized

```php
public bool $_configDirNormalized
```






***

### _joined_config_dir

joined config directory string used in cache keys

```php
public string $_joined_config_dir
```






***

### default_template_handler_func

default template handler

```php
public callable $default_template_handler_func
```






***

### default_config_handler_func

default config handler

```php
public callable $default_config_handler_func
```






***

### default_plugin_handler_func

default plugin handler

```php
public callable $default_plugin_handler_func
```






***

### _compileDirNormalized

flag if template_dir is normalized

```php
public bool $_compileDirNormalized
```






***

### _pluginsDirNormalized

flag if plugins_dir is normalized

```php
public bool $_pluginsDirNormalized
```






***

### _cacheDirNormalized

flag if template_dir is normalized

```php
public bool $_cacheDirNormalized
```






***

### force_compile

force template compiling?

```php
public bool $force_compile
```






***

### use_sub_dirs

use sub dirs for compiled/cached files?

```php
public bool $use_sub_dirs
```






***

### allow_ambiguous_resources

allow ambiguous resources (that are made unique by the resource handler)

```php
public bool $allow_ambiguous_resources
```






***

### merge_compiled_includes

merge compiled includes

```php
public bool $merge_compiled_includes
```






***

### extends_recursion



```php
public $extends_recursion
```






***

### force_cache

force cache file creation

```php
public bool $force_cache
```






***

### left_delimiter

template left-delimiter

```php
public string $left_delimiter
```






***

### right_delimiter

template right-delimiter

```php
public string $right_delimiter
```






***

### literals

array of strings which shall be treated as literal by compiler

```php
public array $literals
```






***

### security_class

class name
This should be instance of Smarty_Security.

```php
public string $security_class
```





**See Also:**

* \Smarty_Security - 

***

### security_policy

implementation of security class

```php
public \Smarty_Security $security_policy
```






***

### allow_php_templates

controls if the php template file resource is allowed

```php
public bool $allow_php_templates
```






***

### debugging

debug mode
Setting this to true enables the debug-console.

```php
public bool $debugging
```






***

### debugging_ctrl

This determines if debugging is enable-able from the browser.

```php
public string $debugging_ctrl
```

<ul>
 <li>NONE => no debugging control allowed</li>
 <li>URL => enable debugging when SMARTY_DEBUG is found in the URL.</li>
</ul>




***

### smarty_debug_id

Name of debugging URL-param.

```php
public string $smarty_debug_id
```

Only used when $debugging_ctrl is set to 'URL'.
The name of the URL-parameter that activates debugging.




***

### debug_tpl

Path of debug template.

```php
public string $debug_tpl
```






***

### error_reporting

When set, smarty uses this value as error_reporting-level.

```php
public int $error_reporting
```






***

### config_overwrite

Controls whether variables with the same name overwrite each other.

```php
public bool $config_overwrite
```






***

### config_booleanize

Controls whether config values of on/true/yes and off/false/no get converted to boolean.

```php
public bool $config_booleanize
```






***

### config_read_hidden

Controls whether hidden config sections/vars are read from the file.

```php
public bool $config_read_hidden
```






***

### compile_locking

locking concurrent compiles

```php
public bool $compile_locking
```






***

### cache_locking

Controls whether cache resources should use locking mechanism

```php
public bool $cache_locking
```






***

### locking_timeout

seconds to wait for acquiring a lock before ignoring the write lock

```php
public float $locking_timeout
```






***

### default_resource_type

resource type used if none given
Must be an valid key of $registered_resources.

```php
public string $default_resource_type
```






***

### caching_type

caching type
Must be an element of $cache_resource_types.

```php
public string $caching_type
```






***

### default_config_type

config type

```php
public string $default_config_type
```






***

### cache_modified_check

check If-Modified-Since headers

```php
public bool $cache_modified_check
```






***

### registered_plugins

registered plugins

```php
public array $registered_plugins
```






***

### registered_objects

registered objects

```php
public array $registered_objects
```






***

### registered_classes

registered classes

```php
public array $registered_classes
```






***

### registered_filters

registered filters

```php
public array $registered_filters
```






***

### registered_resources

registered resources

```php
public array $registered_resources
```






***

### registered_cache_resources

registered cache resources

```php
public array $registered_cache_resources
```






***

### autoload_filters

autoload filter

```php
public array $autoload_filters
```






***

### default_modifiers

default modifier

```php
public array $default_modifiers
```






***

### escape_html

autoescape variable output

```php
public bool $escape_html
```






***

### start_time

start time for execution time calculation

```php
public int $start_time
```






***

### _current_file

required by the compiler for BC

```php
public string $_current_file
```






***

### _parserdebug

internal flag to enable parser debugging

```php
public bool $_parserdebug
```






***

### _objType

This object type (Smarty = 1, template = 2, data = 4)

```php
public int $_objType
```






***

### _debug

Debug object

```php
public \Smarty_Internal_Debug $_debug
```






***

### template_dir

template directory

```php
protected array $template_dir
```






***

### _processedTemplateDir

flags for normalized template directory entries

```php
protected array $_processedTemplateDir
```






***

### config_dir

config directory

```php
protected array $config_dir
```






***

### _processedConfigDir

flags for normalized template directory entries

```php
protected array $_processedConfigDir
```






***

### compile_dir

compile directory

```php
protected string $compile_dir
```






***

### plugins_dir

plugins directory

```php
protected array $plugins_dir
```






***

### cache_dir

cache directory

```php
protected string $cache_dir
```






***

### obsoleteProperties

removed properties

```php
protected string[] $obsoleteProperties
```






***

### accessMap

List of private properties which will call getter/setter on a direct access

```php
protected string[] $accessMap
```






***

### isMutingUndefinedOrNullWarnings

PHP7 Compatibility mode

```php
private bool $isMutingUndefinedOrNullWarnings
```






***

## Methods


### __construct

Initialize new Smarty object

```php
public __construct(): mixed
```












***

### templateExists

Check if a template resource exists

```php
public templateExists(string $resource_name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$resource_name` | **string** | template name |


**Return Value:**

status



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### enableSecurity

Loads security class and enables security

```php
public enableSecurity(string|\Smarty_Security $security_class = null): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$security_class` | **string&#124;\Smarty_Security** | if a string is used, it must be class-name |


**Return Value:**

current Smarty instance for chaining



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### disableSecurity

Disable security

```php
public disableSecurity(): \Smarty
```









**Return Value:**

current Smarty instance for chaining




***

### addTemplateDir

Add template directory(s)

```php
public addTemplateDir(string|array $template_dir, string $key = null, bool $isConfig = false): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template_dir` | **string&#124;array** | directory(s) of template sources |
| `$key` | **string** | of the array element to assign the template dir to |
| `$isConfig` | **bool** | true for config_dir |


**Return Value:**

current Smarty instance for chaining




***

### getTemplateDir

Get template directories

```php
public getTemplateDir(mixed $index = null, bool $isConfig = false): array|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** | index of directory to get, null to get all |
| `$isConfig` | **bool** | true for config_dir |


**Return Value:**

list of template directories, or directory of $index




***

### setTemplateDir

Set template directory

```php
public setTemplateDir(string|array $template_dir, bool $isConfig = false): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template_dir` | **string&#124;array** | directory(s) of template sources |
| `$isConfig` | **bool** | true for config_dir |


**Return Value:**

current Smarty instance for chaining




***

### addConfigDir

Add config directory(s)

```php
public addConfigDir(string|array $config_dir, mixed $key = null): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config_dir` | **string&#124;array** | directory(s) of config sources |
| `$key` | **mixed** | key of the array element to assign the config dir to |


**Return Value:**

current Smarty instance for chaining




***

### getConfigDir

Get config directory

```php
public getConfigDir(mixed $index = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** | index of directory to get, null to get all |


**Return Value:**

configuration directory




***

### setConfigDir

Set config directory

```php
public setConfigDir(mixed $config_dir): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config_dir` | **mixed** |  |


**Return Value:**

current Smarty instance for chaining




***

### addPluginsDir

Adds directory of plugin files

```php
public addPluginsDir(null|array|string $plugins_dir): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plugins_dir` | **null&#124;array&#124;string** |  |


**Return Value:**

current Smarty instance for chaining




***

### getPluginsDir

Get plugin directories

```php
public getPluginsDir(): array
```









**Return Value:**

list of plugin directories




***

### setPluginsDir

Set plugins directory

```php
public setPluginsDir(string|array $plugins_dir): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plugins_dir` | **string&#124;array** | directory(s) of plugins |


**Return Value:**

current Smarty instance for chaining




***

### getCompileDir

Get compiled directory

```php
public getCompileDir(): string
```









**Return Value:**

path to compiled templates




***

### setCompileDir



```php
public setCompileDir(string $compile_dir): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compile_dir` | **string** | directory to store compiled templates in |


**Return Value:**

current Smarty instance for chaining




***

### getCacheDir

Get cache directory

```php
public getCacheDir(): string
```









**Return Value:**

path of cache directory




***

### setCacheDir

Set cache directory

```php
public setCacheDir(string $cache_dir): \Smarty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cache_dir` | **string** | directory to store cached templates in |


**Return Value:**

current Smarty instance for chaining




***

### createTemplate

creates a template object

```php
public createTemplate(string $template, mixed $cache_id = null, mixed $compile_id = null, object $parent = null, bool $do_clone = true): \Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **string** | the resource handle of the template file |
| `$cache_id` | **mixed** | cache id to be used with this template |
| `$compile_id` | **mixed** | compile id to be used with this template |
| `$parent` | **object** | next higher level of Smarty variables |
| `$do_clone` | **bool** | flag is Smarty object shall be cloned |


**Return Value:**

template object



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### loadPlugin

Takes unknown classes and loads plugin files for them
class name format: Smarty_PluginType_PluginName
plugin filename format: plugintype.pluginname.php

```php
public loadPlugin(string $plugin_name, bool $check = true): string|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plugin_name` | **string** | class plugin name to load |
| `$check` | **bool** | check if already loaded |


**Return Value:**

filepath of loaded file or false



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### _getTemplateId

Get unique template id

```php
public _getTemplateId(string $template_name, null|mixed $cache_id = null, null|mixed $compile_id = null, null $caching = null, \Smarty_Internal_Template $template = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template_name` | **string** |  |
| `$cache_id` | **null&#124;mixed** |  |
| `$compile_id` | **null&#124;mixed** |  |
| `$caching` | **null** |  |
| `$template` | **\Smarty_Internal_Template** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### _realpath

Normalize path
 - remove /./ and /../
 - make it absolute if required

```php
public _realpath(string $path, bool $realpath = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** | file path |
| `$realpath` | **bool** | if true - convert to absolute<br />false - convert to relative<br />null - keep as it is but<br />remove /./ /../ |





***

### _clearTemplateCache

Empty template objects cache

```php
public _clearTemplateCache(): mixed
```












***

### setUseSubDirs



```php
public setUseSubDirs(bool $use_sub_dirs): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$use_sub_dirs` | **bool** |  |





***

### setErrorReporting



```php
public setErrorReporting(int $error_reporting): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error_reporting` | **int** |  |





***

### setEscapeHtml



```php
public setEscapeHtml(bool $escape_html): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$escape_html` | **bool** |  |





***

### getAutoLiteral

Return auto_literal flag

```php
public getAutoLiteral(): bool
```












***

### setAutoLiteral

Set auto_literal flag

```php
public setAutoLiteral(bool $auto_literal = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$auto_literal` | **bool** |  |





***

### setForceCompile



```php
public setForceCompile(bool $force_compile): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$force_compile` | **bool** |  |





***

### setMergeCompiledIncludes



```php
public setMergeCompiledIncludes(bool $merge_compiled_includes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$merge_compiled_includes` | **bool** |  |





***

### getLeftDelimiter

Get left delimiter

```php
public getLeftDelimiter(): string
```












***

### setLeftDelimiter

Set left delimiter

```php
public setLeftDelimiter(string $left_delimiter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left_delimiter` | **string** |  |





***

### getRightDelimiter

Get right delimiter

```php
public getRightDelimiter(): string
```









**Return Value:**

$right_delimiter




***

### setRightDelimiter

Set right delimiter

```php
public setRightDelimiter(mixed $right_delimiter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$right_delimiter` | **mixed** |  |





***

### setDebugging



```php
public setDebugging(bool $debugging): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$debugging` | **bool** |  |





***

### setConfigOverwrite



```php
public setConfigOverwrite(bool $config_overwrite): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config_overwrite` | **bool** |  |





***

### setConfigBooleanize



```php
public setConfigBooleanize(bool $config_booleanize): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config_booleanize` | **bool** |  |





***

### setConfigReadHidden



```php
public setConfigReadHidden(bool $config_read_hidden): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config_read_hidden` | **bool** |  |





***

### setCompileLocking



```php
public setCompileLocking(bool $compile_locking): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compile_locking` | **bool** |  |





***

### setDefaultResourceType



```php
public setDefaultResourceType(string $default_resource_type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$default_resource_type` | **string** |  |





***

### setCachingType



```php
public setCachingType(string $caching_type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caching_type` | **string** |  |





***

### testInstall

Test install

```php
public testInstall(null& $errors = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$errors` | **null** |  |





***

### _getSmartyObj

Get Smarty object

```php
public _getSmartyObj(): \Smarty
```












***

### __get

<<magic>> Generic getter.

```php
public __get(string $name): mixed
```

Calls the appropriate getter function.
Issues an E_USER_NOTICE if no valid getter is found.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | property name |





***

### __set

<<magic>> Generic setter.

```php
public __set(string $name, mixed $value): mixed
```

Calls the appropriate setter function.
Issues an E_USER_NOTICE if no valid setter is found.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | property name |
| `$value` | **mixed** | parameter passed to setter |





***

### _normalizeDir

Normalize and set directory string

```php
private _normalizeDir(string $dirName, string $dir): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dirName` | **string** | cache_dir or compile_dir |
| `$dir` | **string** | filepath of folder |





***

### _normalizeTemplateConfig

Normalize template_dir or config_dir

```php
private _normalizeTemplateConfig(bool $isConfig): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$isConfig` | **bool** | true for config_dir |





***

### muteUndefinedOrNullWarnings

Mutes errors for "undefined index", "undefined array key" and "trying to read property of null".

```php
public muteUndefinedOrNullWarnings(): void
```












***

### isMutingUndefinedOrNullWarnings

Indicates if Smarty will mute errors for "undefined index", "undefined array key" and "trying to read property of null".

```php
public isMutingUndefinedOrNullWarnings(): bool
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
