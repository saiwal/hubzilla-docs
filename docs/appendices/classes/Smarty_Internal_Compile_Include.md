
# Smarty_Internal_Compile_Include

Smarty Internal Plugin Compile Include Class



* Full name: `\Smarty_Internal_Compile_Include`
* Parent class: [`\Smarty_Internal_CompileBase`](./Smarty_Internal_CompileBase.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`CACHING_NOCACHE_CODE`|public| |9999|

## Properties


### required_attributes

Attribute definition: Overwrites base class.

```php
public array $required_attributes
```





**See Also:**

* \Smarty_Internal_CompileBase - 

***

### shorttag_order

Attribute definition: Overwrites base class.

```php
public array $shorttag_order
```





**See Also:**

* \Smarty_Internal_CompileBase - 

***

### option_flags

Attribute definition: Overwrites base class.

```php
public array $option_flags
```





**See Also:**

* \Smarty_Internal_CompileBase - 

***

### optional_attributes

Attribute definition: Overwrites base class.

```php
public array $optional_attributes
```





**See Also:**

* \Smarty_Internal_CompileBase - 

***

### valid_scopes

Valid scope names

```php
public array $valid_scopes
```






***

## Methods


### compile

Compiles code for the {include} tag

```php
public compile(array $args, \Smarty_Internal_SmartyTemplateCompiler $compiler): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** | array with attributes from parser |
| `$compiler` | **\Smarty_Internal_SmartyTemplateCompiler** | compiler object |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyCompilerException`](./SmartyCompilerException.md)

- [`SmartyException`](./SmartyException.md)



***

### compileInlineTemplate

Compile inline sub template

```php
public compileInlineTemplate(\Smarty_Internal_SmartyTemplateCompiler $compiler, \Smarty_Internal_Template $tpl, string $t_hash): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_SmartyTemplateCompiler** |  |
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$t_hash` | **string** |  |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



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


***
> Automatically generated on 2025-03-18
