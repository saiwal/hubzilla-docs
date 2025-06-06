
# Smarty_Internal_Compile_Break

Smarty Internal Plugin Compile Break Class



* Full name: `\Smarty_Internal_Compile_Break`
* Parent class: [`\Smarty_Internal_CompileBase`](./Smarty_Internal_CompileBase.md)



## Properties


### optional_attributes

Attribute definition: Overwrites base class.

```php
public array $optional_attributes
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

### tag

Tag name may be overloaded by Smarty_Internal_Compile_Continue

```php
public string $tag
```






***

## Methods


### compile

Compiles code for the {break} tag

```php
public compile(array $args, \Smarty_Internal_TemplateCompilerBase $compiler): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** | array with attributes from parser |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** | compiler object |


**Return Value:**

compiled code



**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***

### checkLevels

check attributes and return array of break and foreach levels

```php
public checkLevels(array $args, \Smarty_Internal_TemplateCompilerBase $compiler): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** | array with attributes from parser |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** | compiler object |




**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



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
