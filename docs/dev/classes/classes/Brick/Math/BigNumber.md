
# BigNumber

Common interface for arbitrary-precision rational numbers.



* Full name: `\Brick\Math\BigNumber`
* This class implements:
[`\Serializable`](../../Serializable.md), [`\JsonSerializable`](../../JsonSerializable.md)
* This class is an **Abstract class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`PARSE_REGEXP`|private| |&#039;/^&#039; . &#039;(?&lt;sign&gt;[\-\+])?&#039; . &#039;(?:&#039; . &#039;(?:&#039; . &#039;(?&lt;integral&gt;[0-9]+)?&#039; . &#039;(?&lt;point&gt;\.)?&#039; . &#039;(?&lt;fractional&gt;[0-9]+)?&#039; . &#039;(?:[eE](?&lt;exponent&gt;[\-\+]?[0-9]+))?&#039; . &#039;)|(?:&#039; . &#039;(?&lt;numerator&gt;[0-9]+)&#039; . &#039;\/?&#039; . &#039;(?&lt;denominator&gt;[0-9]+)&#039; . &#039;)&#039; . &#039;)&#039; . &#039;$/&#039;|


## Methods


### of

Creates a BigNumber of the given value.

```php
public static of(\Brick\Math\BigNumber|int|float|string $value): \Brick\Math\BigNumber
```

The concrete return type is dependent on the given value, with the following rules:

- BigNumber instances are returned as is
- integer numbers are returned as BigInteger
- floating point numbers are converted to a string then parsed as such
- strings containing a `/` character are returned as BigRational
- strings containing a `.` character or using an exponential notation are returned as BigDecimal
- strings containing only digits with an optional leading `+` or `-` sign are returned as BigInteger

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |




**Throws:**
<p>If the format of the number is not valid.</p>

- [`NumberFormatException`](./Exception/NumberFormatException.md)
<p>If the value represents a rational number with a denominator of zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### floatToString

Safely converts float to string, avoiding locale-dependent issues.

```php
private static floatToString(float $float): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$float` | **float** |  |





**See Also:**

* https://github.com/brick/math/pull/20 - 

***

### min

Returns the minimum of the given values.

```php
public static min(\Brick\Math\BigNumber|int|float|string $values): static
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$values` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The numbers to compare. All the numbers need to be convertible<br />to an instance of the class this method is called on. |




**Throws:**
<p>If no values are given.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)
<p>If an argument is not valid.</p>

- [`MathException`](./Exception/MathException.md)



***

### max

Returns the maximum of the given values.

```php
public static max(\Brick\Math\BigNumber|int|float|string $values): static
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$values` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The numbers to compare. All the numbers need to be convertible<br />to an instance of the class this method is called on. |




**Throws:**
<p>If no values are given.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)
<p>If an argument is not valid.</p>

- [`MathException`](./Exception/MathException.md)



***

### sum

Returns the sum of the given values.

```php
public static sum(\Brick\Math\BigNumber|int|float|string $values): static
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$values` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The numbers to add. All the numbers need to be convertible<br />to an instance of the class this method is called on. |




**Throws:**
<p>If no values are given.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)
<p>If an argument is not valid.</p>

- [`MathException`](./Exception/MathException.md)



***

### add

Adds two BigNumber instances in the correct order to avoid a RoundingNecessaryException.

```php
private static add(\Brick\Math\BigNumber $a, \Brick\Math\BigNumber $b): \Brick\Math\BigNumber
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **\Brick\Math\BigNumber** |  |
| `$b` | **\Brick\Math\BigNumber** |  |





***

### cleanUp

Removes optional leading zeros and + sign from the given number.

```php
private static cleanUp(string $number): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number, validated as a non-empty string of digits with optional leading sign. |





***

### isEqualTo

Checks if this number is equal to the given one.

```php
public isEqualTo(\Brick\Math\BigNumber|int|float|string $that): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |





***

### isLessThan

Checks if this number is strictly lower than the given one.

```php
public isLessThan(\Brick\Math\BigNumber|int|float|string $that): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |





***

### isLessThanOrEqualTo

Checks if this number is lower than or equal to the given one.

```php
public isLessThanOrEqualTo(\Brick\Math\BigNumber|int|float|string $that): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |





***

### isGreaterThan

Checks if this number is strictly greater than the given one.

```php
public isGreaterThan(\Brick\Math\BigNumber|int|float|string $that): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |





***

### isGreaterThanOrEqualTo

Checks if this number is greater than or equal to the given one.

```php
public isGreaterThanOrEqualTo(\Brick\Math\BigNumber|int|float|string $that): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |





***

### isZero

Checks if this number equals zero.

```php
public isZero(): bool
```












***

### isNegative

Checks if this number is strictly negative.

```php
public isNegative(): bool
```












***

### isNegativeOrZero

Checks if this number is negative or zero.

```php
public isNegativeOrZero(): bool
```












***

### isPositive

Checks if this number is strictly positive.

```php
public isPositive(): bool
```












***

### isPositiveOrZero

Checks if this number is positive or zero.

```php
public isPositiveOrZero(): bool
```












***

### getSign

Returns the sign of this number.

```php
public getSign(): int
```




* This method is **abstract**.




**Return Value:**

-1 if the number is negative, 0 if zero, 1 if positive.




***

### compareTo

Compares this number to the given one.

```php
public compareTo(\Brick\Math\BigNumber|int|float|string $that): int
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |


**Return Value:**

[-1,0,1] If `$this` is lower than, equal to, or greater than `$that`.



**Throws:**
<p>If the number is not valid.</p>

- [`MathException`](./Exception/MathException.md)



***

### toBigInteger

Converts this number to a BigInteger.

```php
public toBigInteger(): \Brick\Math\BigInteger
```




* This method is **abstract**.






**Throws:**
<p>If this number cannot be converted to a BigInteger without rounding.</p>

- [`RoundingNecessaryException`](./Exception/RoundingNecessaryException.md)



***

### toBigDecimal

Converts this number to a BigDecimal.

```php
public toBigDecimal(): \Brick\Math\BigDecimal
```




* This method is **abstract**.






**Throws:**
<p>If this number cannot be converted to a BigDecimal without rounding.</p>

- [`RoundingNecessaryException`](./Exception/RoundingNecessaryException.md)



***

### toBigRational

Converts this number to a BigRational.

```php
public toBigRational(): \Brick\Math\BigRational
```




* This method is **abstract**.







***

### toScale

Converts this number to a BigDecimal with the given scale, using rounding if necessary.

```php
public toScale(int $scale, int $roundingMode = RoundingMode::UNNECESSARY): \Brick\Math\BigDecimal
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scale` | **int** | The scale of the resulting `BigDecimal`. |
| `$roundingMode` | **int** | A `RoundingMode` constant. |




**Throws:**
<p>If this number cannot be converted to the given scale without rounding.
This only applies when RoundingMode::UNNECESSARY is used.</p>

- [`RoundingNecessaryException`](./Exception/RoundingNecessaryException.md)



***

### toInt

Returns the exact value of this number as a native integer.

```php
public toInt(): int
```

If this number cannot be converted to a native integer without losing precision, an exception is thrown.
Note that the acceptable range for an integer depends on the platform and differs for 32-bit and 64-bit.


* This method is **abstract**.






**Throws:**
<p>If this number cannot be exactly converted to a native integer.</p>

- [`MathException`](./Exception/MathException.md)



***

### toFloat

Returns an approximation of this number as a floating-point value.

```php
public toFloat(): float
```

Note that this method can discard information as the precision of a floating-point value
is inherently limited.

If the number is greater than the largest representable floating point number, positive infinity is returned.
If the number is less than the smallest representable floating point number, negative infinity is returned.


* This method is **abstract**.







***

### __toString

Returns a string representation of this number.

```php
public __toString(): string
```

The output of this method can be parsed by the `of()` factory method;
this will yield an object equal to this one, without any information loss.


* This method is **abstract**.







***

### jsonSerialize



```php
public jsonSerialize(): string
```












***


***
> Automatically generated on 2025-03-15
