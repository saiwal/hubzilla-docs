***

# HTMLPurifier_ConfigSchema_ValidatorAtom

Fluent interface for validating the contents of member variables.

This should be immutable. See HTMLPurifier_ConfigSchema_Validator for
use-cases. We name this an 'atom' because it's ONLY for validations that
are independent and usually scalar.

* Full name: `\HTMLPurifier_ConfigSchema_ValidatorAtom`



## Properties


### context



```php
protected $context
```






***

### obj



```php
protected $obj
```






***

### member



```php
protected $member
```






***

### contents



```php
protected $contents
```






***

## Methods


### __construct



```php
public __construct(mixed $context, mixed $obj, mixed $member): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$context` | **mixed** |  |
| `$obj` | **mixed** |  |
| `$member` | **mixed** |  |





***

### assertIsString



```php
public assertIsString(): \HTMLPurifier_ConfigSchema_ValidatorAtom
```












***

### assertIsBool



```php
public assertIsBool(): \HTMLPurifier_ConfigSchema_ValidatorAtom
```












***

### assertIsArray



```php
public assertIsArray(): \HTMLPurifier_ConfigSchema_ValidatorAtom
```












***

### assertNotNull



```php
public assertNotNull(): \HTMLPurifier_ConfigSchema_ValidatorAtom
```












***

### assertAlnum



```php
public assertAlnum(): \HTMLPurifier_ConfigSchema_ValidatorAtom
```












***

### assertNotEmpty



```php
public assertNotEmpty(): \HTMLPurifier_ConfigSchema_ValidatorAtom
```












***

### assertIsLookup



```php
public assertIsLookup(): \HTMLPurifier_ConfigSchema_ValidatorAtom
```












***

### error



```php
protected error(string $msg): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **string** |  |




**Throws:**

- [`HTMLPurifier_ConfigSchema_Exception`](./HTMLPurifier_ConfigSchema_Exception.md)



***


***
> Automatically generated on 2025-03-15
