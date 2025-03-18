
# Smarty_Internal_Undefined

Smarty Internal Undefined

Class to handle undefined method calls or calls to obsolete runtime extensions

* Full name: `\Smarty_Internal_Undefined`



## Properties


### class

Name of undefined extension class

```php
public string|null $class
```






***

## Methods


### __construct

Smarty_Internal_Undefined constructor.

```php
public __construct(null|string $class = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **null&#124;string** | name of undefined extension class |





***

### decodeProperties

Wrapper for obsolete class Smarty_Internal_Runtime_ValidateCompiled

```php
public decodeProperties(\Smarty_Internal_Template $tpl, array $properties, bool $cache = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$properties` | **array** | special template properties |
| `$cache` | **bool** | flag if called from cache file |


**Return Value:**

false




***

### __call

Call error handler for undefined method

```php
public __call(string $name, array $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | unknown method-name |
| `$args` | **array** | argument array |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-18
