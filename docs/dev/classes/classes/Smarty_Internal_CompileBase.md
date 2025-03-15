
# Smarty_Internal_CompileBase

This class does extend all internal compile plugins



* Full name: `\Smarty_Internal_CompileBase`
* This class is an **Abstract class**



## Properties


### required_attributes

Array of names of required attribute required by tag

```php
public array $required_attributes
```






***

### optional_attributes

Array of names of optional attribute required by tag
use array('_any') if there is no restriction of attributes names

```php
public array $optional_attributes
```






***

### shorttag_order

Shorttag attribute order defined by its names

```php
public array $shorttag_order
```






***

### option_flags

Array of names of valid option flags

```php
public array $option_flags
```






***

### optionMap

Mapping array for boolean option value

```php
public array $optionMap
```






***

### mapCache

Mapping array with attributes as key

```php
public array $mapCache
```






***

## Methods


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
