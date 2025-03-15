
# Smarty_Internal_Compile_Foreach

Smarty Internal Plugin Compile Foreach Class



* Full name: `\Smarty_Internal_Compile_Foreach`
* Parent class: [`\Smarty_Internal_Compile_Private_ForeachSection`](./Smarty_Internal_Compile_Private_ForeachSection.md)



## Properties


### required_attributes

Attribute definition: Overwrites base class.

```php
public array $required_attributes
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

### shorttag_order

Attribute definition: Overwrites base class.

```php
public array $shorttag_order
```





**See Also:**

* \Smarty_Internal_CompileBase - 

***

### counter

counter

```php
public int $counter
```






***

### tagName

Name of this tag

```php
public string $tagName
```






***

### nameProperties

Valid properties of $smarty.foreach.name.xxx variable

```php
public array $nameProperties
```






***

### itemProperties

Valid properties of $item@xxx variable

```php
public array $itemProperties
```






***

### isNamed

Flag if tag had name attribute

```php
public bool $isNamed
```






***

## Methods


### compile

Compiles code for the {foreach} tag

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

- [`SmartyException`](./SmartyException.md)



***

### compileRestore

Compiles code for to restore saved template variables

```php
public compileRestore(int $levels): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$levels` | **int** | number of levels to restore |


**Return Value:**

compiled code




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

### scanForProperties

Scan sources for used tag attributes

```php
public scanForProperties(array $attributes, \Smarty_Internal_TemplateCompilerBase $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attributes` | **array** |  |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### buildPropertyPreg

Build property preg string

```php
public buildPropertyPreg(bool $named, array $attributes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$named` | **bool** |  |
| `$attributes` | **array** |  |





***

### matchProperty

Find matches in source string

```php
public matchProperty(string $source): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |





***

### matchTemplateSource

Find matches in template source

```php
public matchTemplateSource(\Smarty_Internal_TemplateCompilerBase $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |





***

### matchParentTemplateSource

Find matches in all parent template source

```php
public matchParentTemplateSource(\Smarty_Internal_TemplateCompilerBase $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### matchBlockSource

Find matches in {block} tag source

```php
public matchBlockSource(\Smarty_Internal_TemplateCompilerBase $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |





***

### compileSpecialVariable

Compiles code for the {$smarty.foreach.xxx} or {$smarty.section.xxx}tag

```php
public compileSpecialVariable(array $args, \Smarty_Internal_TemplateCompilerBase $compiler, array $parameter): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** | array with attributes from parser |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** | compiler object |
| `$parameter` | **array** | array with compilation parameter |


**Return Value:**

compiled code



**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***


***
> Automatically generated on 2025-03-15
