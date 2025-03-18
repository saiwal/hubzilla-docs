
# CalculatorInterface

A calculator performs arithmetic operations on numbers



* Full name: `\Ramsey\Uuid\Math\CalculatorInterface`



## Methods


### add

Returns the sum of all the provided parameters

```php
public add(\Ramsey\Uuid\Type\NumberInterface $augend, \Ramsey\Uuid\Type\NumberInterface $addends): \Ramsey\Uuid\Type\NumberInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$augend` | **\Ramsey\Uuid\Type\NumberInterface** | The first addend (the integer being added to) |
| `$addends` | **\Ramsey\Uuid\Type\NumberInterface** | The additional integers to a add to the augend |


**Return Value:**

The sum of all the parameters




***

### subtract

Returns the difference of all the provided parameters

```php
public subtract(\Ramsey\Uuid\Type\NumberInterface $minuend, \Ramsey\Uuid\Type\NumberInterface $subtrahends): \Ramsey\Uuid\Type\NumberInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$minuend` | **\Ramsey\Uuid\Type\NumberInterface** | The integer being subtracted from |
| `$subtrahends` | **\Ramsey\Uuid\Type\NumberInterface** | The integers to subtract from the minuend |


**Return Value:**

The difference after subtracting all parameters




***

### multiply

Returns the product of all the provided parameters

```php
public multiply(\Ramsey\Uuid\Type\NumberInterface $multiplicand, \Ramsey\Uuid\Type\NumberInterface $multipliers): \Ramsey\Uuid\Type\NumberInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$multiplicand` | **\Ramsey\Uuid\Type\NumberInterface** | The integer to be multiplied |
| `$multipliers` | **\Ramsey\Uuid\Type\NumberInterface** | The factors by which to multiply the multiplicand |


**Return Value:**

The product of multiplying all the provided parameters




***

### divide

Returns the quotient of the provided parameters divided left-to-right

```php
public divide(int $roundingMode, int $scale, \Ramsey\Uuid\Type\NumberInterface $dividend, \Ramsey\Uuid\Type\NumberInterface $divisors): \Ramsey\Uuid\Type\NumberInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$roundingMode` | **int** | The RoundingMode constant to use for this operation |
| `$scale` | **int** | The scale to use for this operation |
| `$dividend` | **\Ramsey\Uuid\Type\NumberInterface** | The integer to be divided |
| `$divisors` | **\Ramsey\Uuid\Type\NumberInterface** | The integers to divide $dividend by, in<br />the order in which the division operations should take place<br />(left-to-right) |


**Return Value:**

The quotient of dividing the provided parameters left-to-right




***

### fromBase

Converts a value from an arbitrary base to a base-10 integer value

```php
public fromBase(string $value, int $base): \Ramsey\Uuid\Type\Integer
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** | The value to convert |
| `$base` | **int** | The base to convert from (i.e., 2, 16, 32, etc.) |


**Return Value:**

The base-10 integer value of the converted value




***

### toBase

Converts a base-10 integer value to an arbitrary base

```php
public toBase(\Ramsey\Uuid\Type\Integer $value, int $base): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Ramsey\Uuid\Type\Integer** | The integer value to convert |
| `$base` | **int** | The base to convert to (i.e., 2, 16, 32, etc.) |


**Return Value:**

The value represented in the specified base




***

### toHexadecimal

Converts an Integer instance to a Hexadecimal instance

```php
public toHexadecimal(\Ramsey\Uuid\Type\Integer $value): \Ramsey\Uuid\Type\Hexadecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Ramsey\Uuid\Type\Integer** |  |





***

### toInteger

Converts a Hexadecimal instance to an Integer instance

```php
public toInteger(\Ramsey\Uuid\Type\Hexadecimal $value): \Ramsey\Uuid\Type\Integer
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Ramsey\Uuid\Type\Hexadecimal** |  |





***


***
> Automatically generated on 2025-03-18
