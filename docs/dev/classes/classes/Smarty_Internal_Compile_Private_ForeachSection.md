
# Smarty_Internal_Compile_Private_ForeachSection

Smarty Internal Plugin Compile ForeachSection Class



* Full name: `\Smarty_Internal_Compile_Private_ForeachSection`
* Parent class: [`\Smarty_Internal_CompileBase`](./Smarty_Internal_CompileBase.md)



## Properties


### tagName

Name of this tag

```php
public string $tagName
```






***

### nameProperties

Valid properties of $smarty.xxx variable

```php
public array $nameProperties
```






***

### itemProperties

{section} tag has no item properties

```php
public array $itemProperties
```






***

### isNamed

{section} tag has always name attribute

```php
public bool $isNamed
```






***

### matchResults



```php
public array $matchResults
```






***

### propertyPreg

Preg search pattern

```php
private string $propertyPreg
```






***

### resultOffsets

Offsets in preg match result

```php
private array $resultOffsets
```






***

### startOffset

Start offset

```php
private int $startOffset
```






***

## Methods


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
> Automatically generated on 2025-03-15
