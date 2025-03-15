***

# Smarty_Internal_Method_Literals

Smarty Method GetLiterals

Smarty::getLiterals() method

* Full name: `\Smarty_Internal_Method_Literals`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### getLiterals

Get literals

```php
public getLiterals(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |


**Return Value:**

list of literals




***

### addLiterals

Add literals

```php
public addLiterals(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, array|string $literals = null): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$literals` | **array&#124;string** | literal or list of literals<br />to addto add |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### setLiterals

Set literals

```php
public setLiterals(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, array|string $literals = null): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$literals` | **array&#124;string** | literal or list of literals<br />to setto set |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### set

common setter for literals for easier handling of duplicates the
Smarty::$literals array gets filled with identical key values

```php
private set(\Smarty $smarty, array $literals): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$literals` | **array** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
