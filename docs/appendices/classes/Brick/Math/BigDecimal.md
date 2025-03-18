
# BigDecimal

Immutable, arbitrary-precision signed decimal numbers.



* Full name: `\Brick\Math\BigDecimal`
* Parent class: [`\Brick\Math\BigNumber`](./BigNumber.md)
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### value

The unscaled value of this decimal number.

```php
private string $value
```

This is a string of digits with an optional leading minus sign.
No leading zero must be present.
No leading minus sign must be present if the value is 0.




***

### scale

The scale (number of digits after the decimal point) of this decimal number.

```php
private int $scale
```

This must be zero or more.




***

## Methods


### __construct

Protected constructor. Use a factory method to obtain an instance.

```php
protected __construct(string $value, int $scale): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** | The unscaled value, validated. |
| `$scale` | **int** | The scale, validated. |





***

### of

Creates a BigDecimal of the given value.

```php
public static of(\Brick\Math\BigNumber|int|float|string $value): \Brick\Math\BigDecimal
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |




**Throws:**
<p>If the value cannot be converted to a BigDecimal.</p>

- [`MathException`](./Exception/MathException.md)



***

### ofUnscaledValue

Creates a BigDecimal from an unscaled value and a scale.

```php
public static ofUnscaledValue(\Brick\Math\BigNumber|int|float|string $value, int $scale): \Brick\Math\BigDecimal
```

Example: `(12345, 3)` will result in the BigDecimal `12.345`.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The unscaled value. Must be convertible to a BigInteger. |
| `$scale` | **int** | The scale of the number, positive or zero. |




**Throws:**
<p>If the scale is negative.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### zero

Returns a BigDecimal representing zero, with a scale of zero.

```php
public static zero(): \Brick\Math\BigDecimal
```



* This method is **static**.








***

### one

Returns a BigDecimal representing one, with a scale of zero.

```php
public static one(): \Brick\Math\BigDecimal
```



* This method is **static**.








***

### ten

Returns a BigDecimal representing ten, with a scale of zero.

```php
public static ten(): \Brick\Math\BigDecimal
```



* This method is **static**.








***

### plus

Returns the sum of this number and the given one.

```php
public plus(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigDecimal
```

The result has a scale of `max($this->scale, $that->scale)`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The number to add. Must be convertible to a BigDecimal. |




**Throws:**
<p>If the number is not valid, or is not convertible to a BigDecimal.</p>

- [`MathException`](./Exception/MathException.md)



***

### minus

Returns the difference of this number and the given one.

```php
public minus(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigDecimal
```

The result has a scale of `max($this->scale, $that->scale)`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The number to subtract. Must be convertible to a BigDecimal. |




**Throws:**
<p>If the number is not valid, or is not convertible to a BigDecimal.</p>

- [`MathException`](./Exception/MathException.md)



***

### multipliedBy

Returns the product of this number and the given one.

```php
public multipliedBy(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigDecimal
```

The result has a scale of `$this->scale + $that->scale`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The multiplier. Must be convertible to a BigDecimal. |




**Throws:**
<p>If the multiplier is not a valid number, or is not convertible to a BigDecimal.</p>

- [`MathException`](./Exception/MathException.md)



***

### dividedBy

Returns the result of the division of this number by the given one, at the given scale.

```php
public dividedBy(\Brick\Math\BigNumber|int|float|string $that, int|null $scale = null, int $roundingMode = RoundingMode::UNNECESSARY): \Brick\Math\BigDecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. |
| `$scale` | **int&#124;null** | The desired scale, or null to use the scale of this number. |
| `$roundingMode` | **int** | An optional rounding mode. |




**Throws:**
<p>If the scale or rounding mode is invalid.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)
<p>If the number is invalid, is zero, or rounding was necessary.</p>

- [`MathException`](./Exception/MathException.md)



***

### exactlyDividedBy

Returns the exact result of the division of this number by the given one.

```php
public exactlyDividedBy(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigDecimal
```

The scale of the result is automatically calculated to fit all the fraction digits.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigDecimal. |




**Throws:**
<p>If the divisor is not a valid number, is not convertible to a BigDecimal, is zero,
or the result yields an infinite number of digits.</p>

- [`MathException`](./Exception/MathException.md)



***

### power

Returns this number exponentiated to the given value.

```php
public power(int $exponent): \Brick\Math\BigDecimal
```

The result has a scale of `$this->scale * $exponent`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exponent` | **int** |  |




**Throws:**
<p>If the exponent is not in the range 0 to 1,000,000.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### quotient

Returns the quotient of the division of this number by this given one.

```php
public quotient(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigDecimal
```

The quotient has a scale of `0`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigDecimal. |




**Throws:**
<p>If the divisor is not a valid decimal number, or is zero.</p>

- [`MathException`](./Exception/MathException.md)



***

### remainder

Returns the remainder of the division of this number by this given one.

```php
public remainder(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigDecimal
```

The remainder has a scale of `max($this->scale, $that->scale)`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigDecimal. |




**Throws:**
<p>If the divisor is not a valid decimal number, or is zero.</p>

- [`MathException`](./Exception/MathException.md)



***

### quotientAndRemainder

Returns the quotient and remainder of the division of this number by the given one.

```php
public quotientAndRemainder(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigDecimal[]
```

The quotient has a scale of `0`, and the remainder has a scale of `max($this->scale, $that->scale)`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigDecimal. |


**Return Value:**

An array containing the quotient and the remainder.



**Throws:**
<p>If the divisor is not a valid decimal number, or is zero.</p>

- [`MathException`](./Exception/MathException.md)



***

### sqrt

Returns the square root of this number, rounded down to the given number of decimals.

```php
public sqrt(int $scale): \Brick\Math\BigDecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scale` | **int** |  |




**Throws:**
<p>If the scale is negative.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)
<p>If this number is negative.</p>

- [`NegativeNumberException`](./Exception/NegativeNumberException.md)



***

### withPointMovedLeft

Returns a copy of this BigDecimal with the decimal point moved $n places to the left.

```php
public withPointMovedLeft(int $n): \Brick\Math\BigDecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **int** |  |





***

### withPointMovedRight

Returns a copy of this BigDecimal with the decimal point moved $n places to the right.

```php
public withPointMovedRight(int $n): \Brick\Math\BigDecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **int** |  |





***

### stripTrailingZeros

Returns a copy of this BigDecimal with any trailing zeros removed from the fractional part.

```php
public stripTrailingZeros(): \Brick\Math\BigDecimal
```












***

### abs

Returns the absolute value of this number.

```php
public abs(): \Brick\Math\BigDecimal
```












***

### negated

Returns the negated value of this number.

```php
public negated(): \Brick\Math\BigDecimal
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

### getUnscaledValue



```php
public getUnscaledValue(): \Brick\Math\BigInteger
```












***

### getScale



```php
public getScale(): int
```












***

### getIntegralPart

Returns a string representing the integral part of this decimal number.

```php
public getIntegralPart(): string
```

Example: `-123.456` => `-123`.










***

### getFractionalPart

Returns a string representing the fractional part of this decimal number.

```php
public getFractionalPart(): string
```

If the scale is zero, an empty string is returned.

Examples: `-123.456` => '456', `123` => ''.










***

### hasNonZeroFractionalPart

Returns whether this decimal number has a non-zero fractional part.

```php
public hasNonZeroFractionalPart(): bool
```












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

### scaleValues

Puts the internal values of the given decimal numbers on the same scale.

```php
private scaleValues(\Brick\Math\BigDecimal $x, \Brick\Math\BigDecimal $y): array{: string, : string}
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **\Brick\Math\BigDecimal** |  |
| `$y` | **\Brick\Math\BigDecimal** |  |


**Return Value:**

The scaled integer values of $x and $y.




***

### valueWithMinScale



```php
private valueWithMinScale(int $scale): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scale` | **int** |  |





***

### getUnscaledValueWithLeadingZeros

Adds leading zeros if necessary to the unscaled value to represent the full decimal number.

```php
private getUnscaledValueWithLeadingZeros(): string
```












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
> Automatically generated on 2025-03-18
