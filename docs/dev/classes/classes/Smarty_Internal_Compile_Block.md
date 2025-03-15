***

# Smarty_Internal_Compile_Block

Smarty Internal Plugin Compile Block Class



* Full name: `\Smarty_Internal_Compile_Block`
* Parent class: [`\Smarty_Internal_Compile_Shared_Inheritance`](./Smarty_Internal_Compile_Shared_Inheritance.md)



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

## Methods


### compile

Compiles code for the {block} tag

```php
public compile(array $args, \Smarty_Internal_TemplateCompilerBase $compiler, array $parameter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** | array with attributes from parser |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** | compiler object |
| `$parameter` | **array** | array with compilation parameter |





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

### postCompile

Compile inheritance initialization code as prefix

```php
public static postCompile(\Smarty_Internal_TemplateCompilerBase $compiler, bool|false $initChildSequence = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |
| `$initChildSequence` | **bool&#124;false** | if true force child template |





***

### registerInit

Register post compile callback to compile inheritance initialization code

```php
public registerInit(\Smarty_Internal_TemplateCompilerBase $compiler, bool|false $initChildSequence = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |
| `$initChildSequence` | **bool&#124;false** | if true force child template |





***


***
> Automatically generated on 2025-03-15
