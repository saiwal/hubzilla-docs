***

# Smarty_Internal_Compile_Private_Registered_Block

Smarty Internal Plugin Compile Registered Block Class



* Full name: `\Smarty_Internal_Compile_Private_Registered_Block`
* Parent class: [`\Smarty_Internal_Compile_Private_Block_Plugin`](./Smarty_Internal_Compile_Private_Block_Plugin.md)




## Methods


### setup

Setup callback, parameter array and nocache mode

```php
public setup(\Smarty_Internal_TemplateCompilerBase $compiler, array $_attr, string $tag, null $function): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |
| `$_attr` | **array** | attributes |
| `$tag` | **string** |  |
| `$function` | **null** |  |





***


## Inherited methods


### getAttributes

This function checks if the attributes passed are valid
The attributes passed for the tag to compile are checked against the list of required and
optional attributes. Required attributes must be present. Optional attributes are check against
the corresponding list. The keyword '_any' specifies that any attribute will be accepted
as valid

```php
public getAttributes(object $compiler, array $attributes): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **object** | compiler object |
| `$attributes` | **array** | attributes applied to the tag |


**Return Value:**

of mapped attributes for further processing




***

### openTag

Push opening tag name on stack
Optionally additional data can be saved on stack

```php
public openTag(object $compiler, string $openTag, mixed $data = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **object** | compiler object |
| `$openTag` | **string** | the opening tag&#039;s name |
| `$data` | **mixed** | optional data saved |





***

### closeTag

Pop closing tag
Raise an error if this stack-top doesn't match with expected opening tags

```php
public closeTag(object $compiler, array|string $expectedTag): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **object** | compiler object |
| `$expectedTag` | **array&#124;string** | the expected opening tag names |


**Return Value:**

any type the opening tag's name or saved data




***

### compile

Compiles code for the execution of block plugin

```php
public compile(array $args, \Smarty_Internal_TemplateCompilerBase $compiler, array $parameter, string $tag, string $function = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** | array with attributes from parser |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** | compiler object |
| `$parameter` | **array** | array with compilation parameter |
| `$tag` | **string** | name of block plugin |
| `$function` | **string** | PHP function name |


**Return Value:**

compiled code



**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)

- [`SmartyException`](./SmartyException.md)



***

### setup

Setup callback and parameter array

```php
public setup(\Smarty_Internal_TemplateCompilerBase $compiler, array $_attr, string $tag, string $function): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |
| `$_attr` | **array** | attributes |
| `$tag` | **string** |  |
| `$function` | **string** |  |





***


***
> Automatically generated on 2025-03-15
