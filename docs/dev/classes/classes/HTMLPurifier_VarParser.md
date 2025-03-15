
# HTMLPurifier_VarParser

Parses string representations into their corresponding native PHP
variable type. The base implementation does a simple type-check.



* Full name: `\HTMLPurifier_VarParser`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`C_STRING`|public| |1|
|`ISTRING`|public| |2|
|`TEXT`|public| |3|
|`ITEXT`|public| |4|
|`C_INT`|public| |5|
|`C_FLOAT`|public| |6|
|`C_BOOL`|public| |7|
|`LOOKUP`|public| |8|
|`ALIST`|public| |9|
|`HASH`|public| |10|
|`C_MIXED`|public| |11|

## Properties


### types

Lookup table of allowed types. Mainly for backwards compatibility, but
also convenient for transforming string type names to the integer constants.

```php
public static $types
```



* This property is **static**.


***

### stringTypes

Lookup table of types that are string, and can have aliases or
allowed value lists.

```php
public static $stringTypes
```



* This property is **static**.


***

## Methods


### parse

Validate a variable according to type.

```php
final public parse(mixed $var, int $type, bool $allow_null = false): string
```

It may return NULL as a valid type if $allow_null is true.



* This method is **final**.


**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** | Variable to validate |
| `$type` | **int** | Type of variable, see HTMLPurifier_VarParser-&gt;types |
| `$allow_null` | **bool** | Whether or not to permit null as a value |


**Return Value:**

Validated and type-coerced variable



**Throws:**

- [`HTMLPurifier_VarParserException`](./HTMLPurifier_VarParserException.md)



***

### parseImplementation

Actually implements the parsing. Base implementation does not
do anything to $var. Subclasses should overload this!

```php
protected parseImplementation(mixed $var, int $type, bool $allow_null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** |  |
| `$type` | **int** |  |
| `$allow_null` | **bool** |  |





***

### error

Throws an exception.

```php
protected error(mixed $msg): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **mixed** |  |




**Throws:**

- [`HTMLPurifier_VarParserException`](./HTMLPurifier_VarParserException.md)



***

### errorInconsistent

Throws an inconsistency exception.

```php
protected errorInconsistent(string $class, int $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** |  |
| `$type` | **int** |  |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### errorGeneric

Generic error for if a type didn't work.

```php
protected errorGeneric(mixed $var, int $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** |  |
| `$type` | **int** |  |





***

### getTypeName



```php
public static getTypeName(int $type): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** |  |





***


***
> Automatically generated on 2025-03-15
