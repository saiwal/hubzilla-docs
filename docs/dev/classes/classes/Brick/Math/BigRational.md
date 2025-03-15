
# BigRational

An arbitrarily large rational number.

This class is immutable.

* Full name: `\Brick\Math\BigRational`
* Parent class: [`\Brick\Math\BigNumber`](./BigNumber.md)
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### numerator

The numerator.

```php
private \Brick\Math\BigInteger $numerator
```






***

### denominator

The denominator. Always strictly positive.

```php
private \Brick\Math\BigInteger $denominator
```






***

## Methods


### __construct

Protected constructor. Use a factory method to obtain an instance.

```php
protected __construct(\Brick\Math\BigInteger $numerator, \Brick\Math\BigInteger $denominator, bool $checkDenominator): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numerator` | **\Brick\Math\BigInteger** | The numerator. |
| `$denominator` | **\Brick\Math\BigInteger** | The denominator. |
| `$checkDenominator` | **bool** | Whether to check the denominator for negative and zero. |




**Throws:**
<p>If the denominator is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### of

Creates a BigRational of the given value.

```php
public static of(\Brick\Math\BigNumber|int|float|string $value): \Brick\Math\BigRational
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |




**Throws:**
<p>If the value cannot be converted to a BigRational.</p>

- [`MathException`](./Exception/MathException.md)



***

### nd

Creates a BigRational out of a numerator and a denominator.

```php
public static nd(\Brick\Math\BigNumber|int|float|string $numerator, \Brick\Math\BigNumber|int|float|string $denominator): \Brick\Math\BigRational
```

If the denominator is negative, the signs of both the numerator and the denominator
will be inverted to ensure that the denominator is always positive.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numerator` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The numerator. Must be convertible to a BigInteger. |
| `$denominator` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The denominator. Must be convertible to a BigInteger. |




**Throws:**
<p>If an argument does not represent a valid number.</p>

- [`NumberFormatException`](./Exception/NumberFormatException.md)
<p>If an argument represents a non-integer number.</p>

- [`RoundingNecessaryException`](./Exception/RoundingNecessaryException.md)
<p>If the denominator is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### zero

Returns a BigRational representing zero.

```php
public static zero(): \Brick\Math\BigRational
```



* This method is **static**.








***

### one

Returns a BigRational representing one.

```php
public static one(): \Brick\Math\BigRational
```



* This method is **static**.








***

### ten

Returns a BigRational representing ten.

```php
public static ten(): \Brick\Math\BigRational
```



* This method is **static**.








***

### getNumerator



```php
public getNumerator(): \Brick\Math\BigInteger
```












***

### getDenominator



```php
public getDenominator(): \Brick\Math\BigInteger
```












***

### quotient

Returns the quotient of the division of the numerator by the denominator.

```php
public quotient(): \Brick\Math\BigInteger
```












***

### remainder

Returns the remainder of the division of the numerator by the denominator.

```php
public remainder(): \Brick\Math\BigInteger
```












***

### quotientAndRemainder

Returns the quotient and remainder of the division of the numerator by the denominator.

```php
public quotientAndRemainder(): \Brick\Math\BigInteger[]
```












***

### plus

Returns the sum of this number and the given one.

```php
public plus(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigRational
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The number to add. |




**Throws:**
<p>If the number is not valid.</p>

- [`MathException`](./Exception/MathException.md)



***

### minus

Returns the difference of this number and the given one.

```php
public minus(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigRational
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The number to subtract. |




**Throws:**
<p>If the number is not valid.</p>

- [`MathException`](./Exception/MathException.md)



***

### multipliedBy

Returns the product of this number and the given one.

```php
public multipliedBy(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigRational
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The multiplier. |




**Throws:**
<p>If the multiplier is not a valid number.</p>

- [`MathException`](./Exception/MathException.md)



***

### dividedBy

Returns the result of the division of this number by the given one.

```php
public dividedBy(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigRational
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. |




**Throws:**
<p>If the divisor is not a valid number, or is zero.</p>

- [`MathException`](./Exception/MathException.md)



***

### power

Returns this number exponentiated to the given value.

```php
public power(int $exponent): \Brick\Math\BigRational
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exponent` | **int** |  |




**Throws:**
<p>If the exponent is not in the range 0 to 1,000,000.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### reciprocal

Returns the reciprocal of this BigRational.

```php
public reciprocal(): \Brick\Math\BigRational
```

The reciprocal has the numerator and denominator swapped.









**Throws:**
<p>If the numerator is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### abs

Returns the absolute value of this BigRational.

```php
public abs(): \Brick\Math\BigRational
```












***

### negated

Returns the negated value of this BigRational.

```php
public negated(): \Brick\Math\BigRational
```












***

### simplified

Returns the simplified value of this BigRational.

```php
public simplified(): \Brick\Math\BigRational
```












***

### compareTo

Compares this number to the given one.

```php
public compareTo(\Brick\Math\BigNumber|int|float|string $that): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |


**Return Value:**

[-1,0,1] If `$this` is lower than, equal to, or greater than `$that`.




***

### getSign

Returns the sign of this number.

```php
public getSign(): int
```









**Return Value:**

-1 if the number is negative, 0 if zero, 1 if positive.




***

### toBigInteger

Converts this number to a BigInteger.

```php
public toBigInteger(): \Brick\Math\BigInteger
```












***

### toBigDecimal

Converts this number to a BigDecimal.

```php
public toBigDecimal(): \Brick\Math\BigDecimal
```












***

### toBigRational

Converts this number to a BigRational.

```php
public toBigRational(): \Brick\Math\BigRational
```












***

### toScale

Converts this number to a BigDecimal with the given scale, using rounding if necessary.

```php
public toScale(int $scale, int $roundingMode = RoundingMode::UNNECESSARY): \Brick\Math\BigDecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scale` | **int** | The scale of the resulting `BigDecimal`. |
| `$roundingMode` | **int** | A `RoundingMode` constant. |





***

### toInt

Returns the exact value of this number as a native integer.

```php
public toInt(): int
```

If this number cannot be converted to a native integer without losing precision, an exception is thrown.
Note that the acceptable range for an integer depends on the platform and differs for 32-bit and 64-bit.










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










***

### __toString

Returns a string representation of this number.

```php
public __toString(): string
```

The output of this method can be parsed by the `of()` factory method;
this will yield an object equal to this one, without any information loss.










***


## Inherited methods


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
