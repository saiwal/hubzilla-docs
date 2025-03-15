***

# Smarty_Internal_Extension_Handler

Smarty Extension handler

Load extensions dynamically

* Full name: `\Smarty_Internal_Extension_Handler`



## Properties


### objType



```php
public $objType
```






***

### _property_info

Cache for property information from generic getter/setter
Preloaded with names which should not use with generic getter/setter

```php
private array $_property_info
```






***

### resolvedProperties



```php
private $resolvedProperties
```






***

## Methods


### _callExternalMethod

Call external Method

```php
public _callExternalMethod(\Smarty_Internal_Data $data, string $name, array $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data** |  |
| `$name` | **string** | external method names |
| `$args` | **array** | argument array |





***

### upperCase

Make first character of name parts upper case

```php
public upperCase(string $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### __get

get extension object

```php
public __get(string $property_name): mixed|\Smarty_Template_Cached
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property_name` | **string** | property name |





***

### __set

set extension property

```php
public __set(string $property_name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property_name` | **string** | property name |
| `$value` | **mixed** | value |





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





***


***
> Automatically generated on 2025-03-15
