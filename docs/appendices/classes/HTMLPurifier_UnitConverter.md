
# HTMLPurifier_UnitConverter

Class for converting between different unit-lengths as specified by
CSS.



* Full name: `\HTMLPurifier_UnitConverter`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`ENGLISH`|public| |1|
|`METRIC`|public| |2|
|`DIGITAL`|public| |3|

## Properties


### units

Units information array. Units are grouped into measuring systems
(English, Metric), and are assigned an integer representing
the conversion factor between that unit and the smallest unit in
the system. Numeric indexes are actually magical constants that
encode conversion data from one system to the next, with a O(n^2)
constraint on memory (this is generally not a problem, since
the number of measuring systems is small.)

```php
protected static $units
```



* This property is **static**.


***

### outputPrecision

Minimum bcmath precision for output.

```php
protected $outputPrecision
```






***

### internalPrecision

Bcmath precision for internal calculations.

```php
protected $internalPrecision
```






***

### bcmath

Whether or not BCMath is available.

```php
private $bcmath
```






***

## Methods


### __construct



```php
public __construct(mixed $output_precision = 4, mixed $internal_precision = 10, mixed $force_no_bcmath = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$output_precision` | **mixed** |  |
| `$internal_precision` | **mixed** |  |
| `$force_no_bcmath` | **mixed** |  |





***

### convert

Converts a length object of one unit into another unit.

```php
public convert(\HTMLPurifier_Length $length, string $to_unit): \HTMLPurifier_Length|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **\HTMLPurifier_Length** | <br />Instance of HTMLPurifier_Length to convert. You must validate()<br />it before passing it here! |
| `$to_unit` | **string** | <br />Unit to convert to. |





***

### getSigFigs

Returns the number of significant figures in a string number.

```php
public getSigFigs(string $n): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **string** | Decimal number |


**Return Value:**

number of sigfigs




***

### add

Adds two numbers, using arbitrary precision when available.

```php
private add(string $s1, string $s2, int $scale): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s1` | **string** |  |
| `$s2` | **string** |  |
| `$scale` | **int** |  |





***

### mul

Multiples two numbers, using arbitrary precision when available.

```php
private mul(string $s1, string $s2, int $scale): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s1` | **string** |  |
| `$s2` | **string** |  |
| `$scale` | **int** |  |





***

### div

Divides two numbers, using arbitrary precision when available.

```php
private div(string $s1, string $s2, int $scale): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s1` | **string** |  |
| `$s2` | **string** |  |
| `$scale` | **int** |  |





***

### round

Rounds a number according to the number of sigfigs it should have,
using arbitrary precision when available.

```php
private round(float $n, int $sigfigs): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **float** |  |
| `$sigfigs` | **int** |  |





***

### scale

Scales a float to $scale digits right of decimal point, like BCMath.

```php
private scale(float $r, int $scale): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$r` | **float** |  |
| `$scale` | **int** |  |





***


***
> Automatically generated on 2025-03-18
