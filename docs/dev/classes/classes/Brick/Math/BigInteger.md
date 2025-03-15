
# BigInteger

An arbitrary-size integer.

All methods accepting a number as a parameter accept either a BigInteger instance,
an integer, or a string representing an arbitrary size integer.

* Full name: `\Brick\Math\BigInteger`
* Parent class: [`\Brick\Math\BigNumber`](./BigNumber.md)
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### value

The value, as a string of digits with optional leading minus sign.

```php
private string $value
```

No leading zeros must be present.
No leading minus sign must be present if the number is zero.




***

## Methods


### __construct

Protected constructor. Use a factory method to obtain an instance.

```php
protected __construct(string $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** | A string of digits, with optional leading minus sign. |





***

### of

Creates a BigInteger of the given value.

```php
public static of(\Brick\Math\BigNumber|int|float|string $value): \Brick\Math\BigInteger
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** |  |




**Throws:**
<p>If the value cannot be converted to a BigInteger.</p>

- [`MathException`](./Exception/MathException.md)



***

### fromBase

Creates a number from a string in a given base.

```php
public static fromBase(string $number, int $base): \Brick\Math\BigInteger
```

The string can optionally be prefixed with the `+` or `-` sign.

Bases greater than 36 are not supported by this method, as there is no clear consensus on which of the lowercase
or uppercase characters should come first. Instead, this method accepts any base up to 36, and does not
differentiate lowercase and uppercase characters, which are considered equal.

For bases greater than 36, and/or custom alphabets, use the fromArbitraryBase() method.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number to convert, in the given base. |
| `$base` | **int** | The base of the number, between 2 and 36. |




**Throws:**
<p>If the number is empty, or contains invalid chars for the given base.</p>

- [`NumberFormatException`](./Exception/NumberFormatException.md)
<p>If the base is out of range.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### fromArbitraryBase

Parses a string containing an integer in an arbitrary base, using a custom alphabet.

```php
public static fromArbitraryBase(string $number, string $alphabet): \Brick\Math\BigInteger
```

Because this method accepts an alphabet with any character, including dash, it does not handle negative numbers.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number to parse. |
| `$alphabet` | **string** | The alphabet, for example &#039;01&#039; for base 2, or &#039;01234567&#039; for base 8. |




**Throws:**
<p>If the given number is empty or contains invalid chars for the given alphabet.</p>

- [`NumberFormatException`](./Exception/NumberFormatException.md)
<p>If the alphabet does not contain at least 2 chars.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### fromBytes

Translates a string of bytes containing the binary representation of a BigInteger into a BigInteger.

```php
public static fromBytes(string $value, bool $signed = true): \Brick\Math\BigInteger
```

The input string is assumed to be in big-endian byte-order: the most significant byte is in the zeroth element.

If `$signed` is true, the input is assumed to be in two's-complement representation, and the leading bit is
interpreted as a sign bit. If `$signed` is false, the input is interpreted as an unsigned number, and the
resulting BigInteger will always be positive or zero.

This method can be used to retrieve a number exported by `toBytes()`, as long as the `$signed` flags match.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** | The byte string. |
| `$signed` | **bool** | Whether to interpret as a signed number in two&#039;s-complement representation with a leading<br />sign bit. |




**Throws:**
<p>If the string is empty.</p>

- [`NumberFormatException`](./Exception/NumberFormatException.md)



***

### randomBits

Generates a pseudo-random number in the range 0 to 2^numBits - 1.

```php
public static randomBits(int $numBits, callable|null $randomBytesGenerator = null): \Brick\Math\BigInteger
```

Using the default random bytes generator, this method is suitable for cryptographic use.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numBits` | **int** | The number of bits. |
| `$randomBytesGenerator` | **callable&#124;null** | A function that accepts a number of bytes as an integer, and returns a<br />string of random bytes of the given length. Defaults to the<br />`random_bytes()` function. |




**Throws:**
<p>If $numBits is negative.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### randomRange

Generates a pseudo-random number between `$min` and `$max`.

```php
public static randomRange(\Brick\Math\BigNumber|int|float|string $min, \Brick\Math\BigNumber|int|float|string $max, callable|null $randomBytesGenerator = null): \Brick\Math\BigInteger
```

Using the default random bytes generator, this method is suitable for cryptographic use.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$min` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The lower bound. Must be convertible to a BigInteger. |
| `$max` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The upper bound. Must be convertible to a BigInteger. |
| `$randomBytesGenerator` | **callable&#124;null** | A function that accepts a number of bytes as an integer,<br />and returns a string of random bytes of the given length.<br />Defaults to the `random_bytes()` function. |




**Throws:**
<p>If one of the parameters cannot be converted to a BigInteger,
or <code class="prettyprint">$min</code> is greater than <code class="prettyprint">$max</code>.</p>

- [`MathException`](./Exception/MathException.md)



***

### zero

Returns a BigInteger representing zero.

```php
public static zero(): \Brick\Math\BigInteger
```



* This method is **static**.








***

### one

Returns a BigInteger representing one.

```php
public static one(): \Brick\Math\BigInteger
```



* This method is **static**.








***

### ten

Returns a BigInteger representing ten.

```php
public static ten(): \Brick\Math\BigInteger
```



* This method is **static**.








***

### gcdMultiple



```php
public static gcdMultiple(\Brick\Math\BigInteger $a, \Brick\Math\BigInteger $n): \Brick\Math\BigInteger
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **\Brick\Math\BigInteger** |  |
| `$n` | **\Brick\Math\BigInteger** |  |





***

### plus

Returns the sum of this number and the given one.

```php
public plus(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The number to add. Must be convertible to a BigInteger. |




**Throws:**
<p>If the number is not valid, or is not convertible to a BigInteger.</p>

- [`MathException`](./Exception/MathException.md)



***

### minus

Returns the difference of this number and the given one.

```php
public minus(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The number to subtract. Must be convertible to a BigInteger. |




**Throws:**
<p>If the number is not valid, or is not convertible to a BigInteger.</p>

- [`MathException`](./Exception/MathException.md)



***

### multipliedBy

Returns the product of this number and the given one.

```php
public multipliedBy(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The multiplier. Must be convertible to a BigInteger. |




**Throws:**
<p>If the multiplier is not a valid number, or is not convertible to a BigInteger.</p>

- [`MathException`](./Exception/MathException.md)



***

### dividedBy

Returns the result of the division of this number by the given one.

```php
public dividedBy(\Brick\Math\BigNumber|int|float|string $that, int $roundingMode = RoundingMode::UNNECESSARY): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigInteger. |
| `$roundingMode` | **int** | An optional rounding mode. |




**Throws:**
<p>If the divisor is not a valid number, is not convertible to a BigInteger, is zero,
or RoundingMode::UNNECESSARY is used and the remainder is not zero.</p>

- [`MathException`](./Exception/MathException.md)



***

### power

Returns this number exponentiated to the given value.

```php
public power(int $exponent): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exponent` | **int** |  |




**Throws:**
<p>If the exponent is not in the range 0 to 1,000,000.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### quotient

Returns the quotient of the division of this number by the given one.

```php
public quotient(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigInteger. |




**Throws:**
<p>If the divisor is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### remainder

Returns the remainder of the division of this number by the given one.

```php
public remainder(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```

The remainder, when non-zero, has the same sign as the dividend.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigInteger. |




**Throws:**
<p>If the divisor is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### quotientAndRemainder

Returns the quotient and remainder of the division of this number by the given one.

```php
public quotientAndRemainder(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigInteger. |


**Return Value:**

An array containing the quotient and the remainder.



**Throws:**
<p>If the divisor is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### mod

Returns the modulo of this number and the given one.

```php
public mod(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```

The modulo operation yields the same result as the remainder operation when both operands are of the same sign,
and may differ when signs are different.

The result of the modulo operation, when non-zero, has the same sign as the divisor.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The divisor. Must be convertible to a BigInteger. |




**Throws:**
<p>If the divisor is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### modInverse

Returns the modular multiplicative inverse of this BigInteger modulo $m.

```php
public modInverse(\Brick\Math\BigInteger $m): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **\Brick\Math\BigInteger** |  |




**Throws:**
<p>If $m is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)
<p>If $m is negative.</p>

- [`NegativeNumberException`](./Exception/NegativeNumberException.md)
<p>If this BigInteger has no multiplicative inverse mod m (that is, this BigInteger
is not relatively prime to m).</p>

- [`MathException`](./Exception/MathException.md)



***

### modPow

Returns this number raised into power with modulo.

```php
public modPow(\Brick\Math\BigNumber|int|float|string $exp, \Brick\Math\BigNumber|int|float|string $mod): \Brick\Math\BigInteger
```

This operation only works on positive numbers.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exp` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The exponent. Must be positive or zero. |
| `$mod` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The modulus. Must be strictly positive. |




**Throws:**
<p>If any of the operands is negative.</p>

- [`NegativeNumberException`](./Exception/NegativeNumberException.md)
<p>If the modulus is zero.</p>

- [`DivisionByZeroException`](./Exception/DivisionByZeroException.md)



***

### gcd

Returns the greatest common divisor of this number and the given one.

```php
public gcd(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```

The GCD is always positive, unless both operands are zero, in which case it is zero.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The operand. Must be convertible to an integer number. |





***

### sqrt

Returns the integer square root number of this number, rounded down.

```php
public sqrt(): \Brick\Math\BigInteger
```

The result is the largest x such that x² ≤ n.









**Throws:**
<p>If this number is negative.</p>

- [`NegativeNumberException`](./Exception/NegativeNumberException.md)



***

### abs

Returns the absolute value of this number.

```php
public abs(): \Brick\Math\BigInteger
```












***

### negated

Returns the inverse of this number.

```php
public negated(): \Brick\Math\BigInteger
```












***

### and

Returns the integer bitwise-and combined with another integer.

```php
public and(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```

This method returns a negative BigInteger if and only if both operands are negative.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The operand. Must be convertible to an integer number. |





***

### or

Returns the integer bitwise-or combined with another integer.

```php
public or(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```

This method returns a negative BigInteger if and only if either of the operands is negative.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The operand. Must be convertible to an integer number. |





***

### xor

Returns the integer bitwise-xor combined with another integer.

```php
public xor(\Brick\Math\BigNumber|int|float|string $that): \Brick\Math\BigInteger
```

This method returns a negative BigInteger if and only if exactly one of the operands is negative.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$that` | **\Brick\Math\BigNumber&#124;int&#124;float&#124;string** | The operand. Must be convertible to an integer number. |





***

### not

Returns the bitwise-not of this BigInteger.

```php
public not(): \Brick\Math\BigInteger
```












***

### shiftedLeft

Returns the integer left shifted by a given number of bits.

```php
public shiftedLeft(int $distance): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$distance` | **int** |  |





***

### shiftedRight

Returns the integer right shifted by a given number of bits.

```php
public shiftedRight(int $distance): \Brick\Math\BigInteger
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$distance` | **int** |  |





***

### getBitLength

Returns the number of bits in the minimal two's-complement representation of this BigInteger, excluding a sign bit.

```php
public getBitLength(): int
```

For positive BigIntegers, this is equivalent to the number of bits in the ordinary binary representation.
Computes (ceil(log2(this < 0 ? -this : this+1))).










***

### getLowestSetBit

Returns the index of the rightmost (lowest-order) one bit in this BigInteger.

```php
public getLowestSetBit(): int
```

Returns -1 if this BigInteger contains no one bits.










***

### isEven

Returns whether this number is even.

```php
public isEven(): bool
```












***

### isOdd

Returns whether this number is odd.

```php
public isOdd(): bool
```












***

### testBit

Returns true if and only if the designated bit is set.

```php
public testBit(int $n): bool
```

Computes ((this & (1<<n)) != 0).






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **int** | The bit to test, 0-based. |




**Throws:**
<p>If the bit to test is negative.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



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

### toBase

Returns a string representation of this number in the given base.

```php
public toBase(int $base): string
```

The output will always be lowercase for bases greater than 10.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base` | **int** |  |




**Throws:**
<p>If the base is out of range.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### toArbitraryBase

Returns a string representation of this number in an arbitrary base with a custom alphabet.

```php
public toArbitraryBase(string $alphabet): string
```

Because this method accepts an alphabet with any character, including dash, it does not handle negative numbers;
a NegativeNumberException will be thrown when attempting to call this method on a negative number.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$alphabet` | **string** | The alphabet, for example &#039;01&#039; for base 2, or &#039;01234567&#039; for base 8. |




**Throws:**
<p>If this number is negative.</p>

- [`NegativeNumberException`](./Exception/NegativeNumberException.md)
<p>If the given alphabet does not contain at least 2 chars.</p>

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### toBytes

Returns a string of bytes containing the binary representation of this BigInteger.

```php
public toBytes(bool $signed = true): string
```

The string is in big-endian byte-order: the most significant byte is in the zeroth element.

If `$signed` is true, the output will be in two's-complement representation, and a sign bit will be prepended to
the output. If `$signed` is false, no sign bit will be prepended, and this method will throw an exception if the
number is negative.

The string will contain the minimum number of bytes required to represent this BigInteger, including a sign bit
if `$signed` is true.

This representation is compatible with the `fromBytes()` factory method, as long as the `$signed` flags match.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$signed` | **bool** | Whether to output a signed number in two&#039;s-complement representation with a leading sign bit. |




**Throws:**
<p>If $signed is false, and the number is negative.</p>

- [`NegativeNumberException`](./Exception/NegativeNumberException.md)



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
