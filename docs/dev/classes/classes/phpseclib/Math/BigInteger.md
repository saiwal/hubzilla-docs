***

# BigInteger

Pure-PHP arbitrary precision integer arithmetic library. Supports base-2, base-10, base-16, and base-256
numbers.



* Full name: `\phpseclib\Math\BigInteger`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`MONTGOMERY`|public| |0|
|`BARRETT`|public| |1|
|`POWEROF2`|public| |2|
|`CLASSIC`|public| |3|
|`NONE`|public| |4|
|`VALUE`|public| |0|
|`SIGN`|public| |1|
|`VARIABLE`|public| |0|
|`DATA`|public| |1|
|`MODE_INTERNAL`|public| |1|
|`MODE_BCMATH`|public| |2|
|`MODE_GMP`|public| |3|
|`KARATSUBA_CUTOFF`|public| |25|

## Properties


### base



```php
public static $base
```



* This property is **static**.


***

### baseFull



```php
public static $baseFull
```



* This property is **static**.


***

### maxDigit



```php
public static $maxDigit
```



* This property is **static**.


***

### msb



```php
public static $msb
```



* This property is **static**.


***

### max10

$max10 in greatest $max10Len satisfying
$max10 = 10**$max10Len <= 2**$base.

```php
public static $max10
```



* This property is **static**.


***

### max10Len

$max10Len in greatest $max10Len satisfying
$max10 = 10**$max10Len <= 2**$base.

```php
public static $max10Len
```



* This property is **static**.


***

### maxDigit2



```php
public static $maxDigit2
```



* This property is **static**.


***

### value

Holds the BigInteger's value.

```php
public array $value
```






***

### is_negative

Holds the BigInteger's magnitude.

```php
public bool $is_negative
```






***

### precision

Precision

```php
public $precision
```





**See Also:**

* \phpseclib\Math\self::setPrecision() - 

***

### bitmask

Precision Bitmask

```php
public $bitmask
```





**See Also:**

* \phpseclib\Math\self::setPrecision() - 

***

### hex

Mode independent value used for serialization.

```php
public string $hex
```

If the bcmath or gmp extensions are installed $this->value will be a non-serializable resource, hence the need for
a variable that'll be serializable regardless of whether or not extensions are being used.  Unlike $this->value,
however, $this->hex is only calculated when $this->__sleep() is called.



**See Also:**

* \phpseclib\Math\self::__sleep() - * \phpseclib\Math\self::__wakeup() - 

***

## Methods


### __construct

Converts base-2, base-10, base-16, and binary strings (base-256) to BigIntegers.

```php
public __construct(int|string|resource $x, int $base = 10): \phpseclib\Math\BigInteger
```

If the second parameter - $base - is negative, then it will be assumed that the number's are encoded using
two's compliment.  The sole exception to this is -10, which is treated the same as 10 is.

Here's an example:
<code>
<?php
   $a = new \phpseclib\Math\BigInteger('0x32', 16); // 50 in base-16

   echo $a->toString(); // outputs 50
?>
</code>






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int&#124;string&#124;resource** | base-10 number or base-$base number if $base set. |
| `$base` | **int** |  |





***

### getLength

Return the size of a BigInteger in bits

```php
public getLength(): int
```












***

### getLengthInBytes

Return the size of a BigInteger in bytes

```php
public getLengthInBytes(): int
```












***

### copy

Copy an object

```php
public copy(): \phpseclib\Math\BigInteger
```

PHP5 passes objects by reference while PHP4 passes by value.  As such, we need a function to guarantee
that all objects are passed by value, when appropriate.  More information can be found here:

{@link http://php.net/language.oop5.basic#51624}










**See Also:**

* \phpseclib\Math\self::__clone() - 

***

### __clone

__clone() magic method

```php
public __clone(): \phpseclib\Math\BigInteger
```

Although you can call BigInteger::__toString() directly in PHP5, you cannot call BigInteger::__clone() directly
in PHP5.  You can in PHP4 since it's not a magic method, but in PHP5, you have to call it by using the PHP5
only syntax of $y = clone $x.  As such, if you're trying to write an application that works on both PHP4 and
PHP5, call BigInteger::copy(), instead.










**See Also:**

* \phpseclib\Math\self::copy() - 

***

### __sleep

__sleep() magic method

```php
public __sleep(): mixed
```

Will be called, automatically, when serialize() is called on a BigInteger object.










**See Also:**

* \phpseclib\Math\self::__wakeup() - 

***

### __wakeup

__wakeup() magic method

```php
public __wakeup(): mixed
```

Will be called, automatically, when unserialize() is called on a BigInteger object.










**See Also:**

* \phpseclib\Math\self::__sleep() - 

***

### __debugInfo

__debugInfo() magic method

```php
public __debugInfo(): mixed
```

Will be called, automatically, when print_r() or var_dump() are called










***

### _add

Performs addition.

```php
public _add(array $x_value, bool $x_negative, array $y_value, bool $y_negative): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_value` | **array** |  |
| `$x_negative` | **bool** |  |
| `$y_value` | **array** |  |
| `$y_negative` | **bool** |  |





***

### _subtract

Performs subtraction.

```php
public _subtract(array $x_value, bool $x_negative, array $y_value, bool $y_negative): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_value` | **array** |  |
| `$x_negative` | **bool** |  |
| `$y_value` | **array** |  |
| `$y_negative` | **bool** |  |





***

### multiply

Multiplies two BigIntegers

```php
public multiply(\phpseclib\Math\BigInteger $x): \phpseclib\Math\BigInteger
```

Here's an example:
<code>
<?php
   $a = new \phpseclib\Math\BigInteger('10');
   $b = new \phpseclib\Math\BigInteger('20');

   $c = $a->multiply($b);

   echo $c->toString(); // outputs 200
?>
</code>






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **\phpseclib\Math\BigInteger** |  |





***

### _multiply

Performs multiplication.

```php
public _multiply(array $x_value, bool $x_negative, array $y_value, bool $y_negative): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_value` | **array** |  |
| `$x_negative` | **bool** |  |
| `$y_value` | **array** |  |
| `$y_negative` | **bool** |  |





***

### _regularMultiply

Performs long multiplication on two BigIntegers

```php
public _regularMultiply(array $x_value, array $y_value): array
```

Modeled after 'multiply' in MutableBigInteger.java.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_value` | **array** |  |
| `$y_value` | **array** |  |





***

### _karatsuba

Performs Karatsuba multiplication on two BigIntegers

```php
public _karatsuba(array $x_value, array $y_value): array
```

See {@link http://en.wikipedia.org/wiki/Karatsuba_algorithm} and
{@link http://math.libtomcrypt.com/files/tommath.pdf#page=120}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_value` | **array** |  |
| `$y_value` | **array** |  |





***

### _square

Performs squaring

```php
public _square(array $x = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |





***

### _baseSquare

Performs traditional squaring on two BigIntegers

```php
public _baseSquare(array $value): array
```

Squaring can be done faster than multiplying a number by itself can be.  See
{@link http://www.cacr.math.uwaterloo.ca/hac/about/chap14.pdf#page=7} /
{@link http://math.libtomcrypt.com/files/tommath.pdf#page=141} for more information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### _karatsubaSquare

Performs Karatsuba "squaring" on two BigIntegers

```php
public _karatsubaSquare(array $value): array
```

See {@link http://en.wikipedia.org/wiki/Karatsuba_algorithm} and
{@link http://math.libtomcrypt.com/files/tommath.pdf#page=151}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### _divide_digit

Divides a BigInteger by a regular integer

```php
public _divide_digit(array $dividend, array $divisor): array
```

abc / x = a00 / x + b0 / x + c / x






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dividend` | **array** |  |
| `$divisor` | **array** |  |





***

### powMod

Performs modular exponentiation.

```php
public powMod(\phpseclib\Math\BigInteger $e, \phpseclib\Math\BigInteger $n): \phpseclib\Math\BigInteger
```

Alias for modPow().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$e` | **\phpseclib\Math\BigInteger** |  |
| `$n` | **\phpseclib\Math\BigInteger** |  |





***

### _slidingWindow

Sliding Window k-ary Modular Exponentiation

```php
public _slidingWindow(\phpseclib\Math\BigInteger $e, \phpseclib\Math\BigInteger $n, int $mode): \phpseclib\Math\BigInteger
```

Based on {@link http://www.cacr.math.uwaterloo.ca/hac/about/chap14.pdf#page=27} /
{@link http://math.libtomcrypt.com/files/tommath.pdf#page=210}.  In a departure from those algorithims,
however, this function performs a modular reduction after every multiplication and squaring operation.
As such, this function has the same preconditions that the reductions being used do.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$e` | **\phpseclib\Math\BigInteger** |  |
| `$n` | **\phpseclib\Math\BigInteger** |  |
| `$mode` | **int** |  |





***

### _reduce

Modular reduction

```php
public _reduce(array $x, array $n, int $mode): array
```

For most $modes this will return the remainder.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$n` | **array** |  |
| `$mode` | **int** |  |





**See Also:**

* \phpseclib\Math\self::_slidingWindow() - 

***

### _prepareReduce

Modular reduction preperation

```php
public _prepareReduce(array $x, array $n, int $mode): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$n` | **array** |  |
| `$mode` | **int** |  |





**See Also:**

* \phpseclib\Math\self::_slidingWindow() - 

***

### _multiplyReduce

Modular multiply

```php
public _multiplyReduce(array $x, array $y, array $n, int $mode): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$y` | **array** |  |
| `$n` | **array** |  |
| `$mode` | **int** |  |





**See Also:**

* \phpseclib\Math\self::_slidingWindow() - 

***

### _squareReduce

Modular square

```php
public _squareReduce(array $x, array $n, int $mode): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$n` | **array** |  |
| `$mode` | **int** |  |





**See Also:**

* \phpseclib\Math\self::_slidingWindow() - 

***

### _mod2

Modulos for Powers of Two

```php
public _mod2(\phpseclib\Math\BigInteger $n): \phpseclib\Math\BigInteger
```

Calculates $x%$n, where $n = 2**$e, for some $e.  Since this is basically the same as doing $x & ($n-1),
we'll just use this function as a wrapper for doing that.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **\phpseclib\Math\BigInteger** |  |





**See Also:**

* \phpseclib\Math\self::_slidingWindow() - 

***

### _barrett

Barrett Modular Reduction

```php
public _barrett(array $n, array $m): array
```

See {@link http://www.cacr.math.uwaterloo.ca/hac/about/chap14.pdf#page=14} /
{@link http://math.libtomcrypt.com/files/tommath.pdf#page=165} for more information.  Modified slightly,
so as not to require negative numbers (initially, this script didn't support negative numbers).

Employs "folding", as described at
{@link http://www.cosic.esat.kuleuven.be/publications/thesis-149.pdf#page=66}.  To quote from
it, "the idea [behind folding] is to find a value x' such that x (mod m) = x' (mod m), with x' being smaller than x."

Unfortunately, the "Barrett Reduction with Folding" algorithm described in thesis-149.pdf is not, as written, all that
usable on account of (1) its not using reasonable radix points as discussed in
{@link http://math.libtomcrypt.com/files/tommath.pdf#page=162} and (2) the fact that, even with reasonable
radix points, it only works when there are an even number of digits in the denominator.  The reason for (2) is that
(x >> 1) + (x >> 1) != x / 2 + x / 2.  If x is even, they're the same, but if x is odd, they're not.  See the in-line
comments for details.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **array** |  |
| `$m` | **array** |  |





**See Also:**

* \phpseclib\Math\self::_slidingWindow() - 

***

### _regularBarrett

(Regular) Barrett Modular Reduction

```php
public _regularBarrett(array $x, array $n): array
```

For numbers with more than four digits BigInteger::_barrett() is faster.  The difference between that and this
is that this function does not fold the denominator into a smaller form.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$n` | **array** |  |





**See Also:**

* \phpseclib\Math\self::_slidingWindow() - 

***

### _multiplyLower

Performs long multiplication up to $stop digits

```php
public _multiplyLower(array $x_value, bool $x_negative, array $y_value, bool $y_negative, int $stop): array
```

If you're going to be doing array_slice($product->value, 0, $stop), some cycles can be saved.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_value` | **array** |  |
| `$x_negative` | **bool** |  |
| `$y_value` | **array** |  |
| `$y_negative` | **bool** |  |
| `$stop` | **int** |  |





**See Also:**

* \phpseclib\Math\self::_regularBarrett() - 

***

### _montgomery

Montgomery Modular Reduction

```php
public _montgomery(array $x, array $n): array
```

($x->_prepMontgomery($n))->_montgomery($n) yields $x % $n.
{@link http://math.libtomcrypt.com/files/tommath.pdf#page=170} provides insights on how this can be
improved upon (basically, by using the comba method).  gcd($n, 2) must be equal to one for this function
to work correctly.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$n` | **array** |  |





**See Also:**

* \phpseclib\Math\self::_prepMontgomery() - * \phpseclib\Math\self::_slidingWindow() - 

***

### _montgomeryMultiply

Montgomery Multiply

```php
public _montgomeryMultiply(array $x, array $y, array $m): array
```

Interleaves the montgomery reduction and long multiplication algorithms together as described in
{@link http://www.cacr.math.uwaterloo.ca/hac/about/chap14.pdf#page=13}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$y` | **array** |  |
| `$m` | **array** |  |





**See Also:**

* \phpseclib\Math\self::_prepMontgomery() - * \phpseclib\Math\self::_montgomery() - 

***

### _prepMontgomery

Prepare a number for use in Montgomery Modular Reductions

```php
public _prepMontgomery(array $x, array $n): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |
| `$n` | **array** |  |





**See Also:**

* \phpseclib\Math\self::_montgomery() - * \phpseclib\Math\self::_slidingWindow() - 

***

### _modInverse67108864

Modular Inverse of a number mod 2**26 (eg. 67108864)

```php
public _modInverse67108864(array $x): int
```

Based off of the bnpInvDigit function implemented and justified in the following URL:

{@link http://www-cs-students.stanford.edu/~tjw/jsbn/jsbn.js}

The following URL provides more info:

{@link http://groups.google.com/group/sci.crypt/msg/7a137205c1be7d85}

As for why we do all the bitmasking...  strange things can happen when converting from floats to ints. For
instance, on some computers, var_dump((int) -4294967297) yields int(-1) and on others, it yields
int(-2147483648).  To avoid problems stemming from this, we use bitmasks to guarantee that ints aren't
auto-converted to floats.  The outermost bitmask is present because without it, there's no guarantee that
the "residue" returned would be the so-called "common residue".  We use fmod, in the last step, because the
maximum possible $x is 26 bits and the maximum $result is 16 bits.  Thus, we have to be able to handle up to
40 bits, which only 64-bit floating points will support.

Thanks to Pedro Gimeno Fortea for input!






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |





**See Also:**

* \phpseclib\Math\self::_montgomery() - 

***

### gcd

Calculates the greatest common divisor

```php
public gcd(\phpseclib\Math\BigInteger $n): \phpseclib\Math\BigInteger
```

Say you have 693 and 609.  The GCD is 21.

Here's an example:
<code>
<?php
   $a = new \phpseclib\Math\BigInteger(693);
   $b = new \phpseclib\Math\BigInteger(609);

   $gcd = a->extendedGCD($b);

   echo $gcd->toString() . "\r\n"; // outputs 21
?>
</code>






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **\phpseclib\Math\BigInteger** |  |





***

### abs

Absolute value.

```php
public abs(): \phpseclib\Math\BigInteger
```












***

### _compare

Compares two numbers.

```php
public _compare(array $x_value, bool $x_negative, array $y_value, bool $y_negative): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_value` | **array** |  |
| `$x_negative` | **bool** |  |
| `$y_value` | **array** |  |
| `$y_negative` | **bool** |  |





**See Also:**

* \phpseclib\Math\self::compare() - 

***

### equals

Tests the equality of two numbers.

```php
public equals(\phpseclib\Math\BigInteger $x): bool
```

If you need to see if one number is greater than or less than another number, use BigInteger::compare()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **\phpseclib\Math\BigInteger** |  |





**See Also:**

* \phpseclib\Math\self::compare() - 

***

### setPrecision

Set Precision

```php
public setPrecision(int $bits): mixed
```

Some bitwise operations give different results depending on the precision being used.  Examples include left
shift, not, and rotates.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bits` | **int** |  |





***

### bitwise_leftRotate

Logical Left Rotate

```php
public bitwise_leftRotate(int $shift): \phpseclib\Math\BigInteger
```

Instead of the top x bits being dropped they're appended to the shifted bit string.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$shift` | **int** |  |





***

### bitwise_rightRotate

Logical Right Rotate

```php
public bitwise_rightRotate(int $shift): \phpseclib\Math\BigInteger
```

Instead of the bottom x bits being dropped they're prepended to the shifted bit string.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$shift` | **int** |  |





***

### _random_number_helper

Generates a random BigInteger

```php
public _random_number_helper(int $size): \phpseclib\Math\BigInteger
```

Byte length is equal to $length. Uses \phpseclib\Crypt\Random if it's loaded and mt_rand if it's not.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$size` | **int** |  |





***

### _make_odd

Make the current number odd

```php
public _make_odd(): mixed
```

If the current number is odd it'll be unchanged.  If it's even, one will be added to it.










**See Also:**

* \phpseclib\Math\self::randomPrime() - 

***

### _lshift

Logical Left Shift

```php
public _lshift(int $shift): mixed
```

Shifts BigInteger's by $shift bits.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$shift` | **int** |  |





***

### _rshift

Logical Right Shift

```php
public _rshift(int $shift): mixed
```

Shifts BigInteger's by $shift bits.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$shift` | **int** |  |





***

### _normalize

Normalize

```php
public _normalize(\phpseclib\Math\BigInteger $result): \phpseclib\Math\BigInteger
```

Removes leading zeros and truncates (if necessary) to maintain the appropriate precision






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$result` | **\phpseclib\Math\BigInteger** |  |





**See Also:**

* \phpseclib\Math\self::_trim() - 

***

### _trim

Trim

```php
public _trim(array $value): \phpseclib\Math\BigInteger
```

Removes leading zeros






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### _array_repeat

Array Repeat

```php
public _array_repeat(array $input, mixed $multiplier): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **array** |  |
| `$multiplier` | **mixed** |  |





***

### _base256_lshift

Logical Left Shift

```php
public _base256_lshift(string& $x, int $shift): string
```

Shifts binary strings $shift bits, essentially multiplying by 2**$shift.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **string** | (by reference) |
| `$shift` | **int** |  |





***

### _base256_rshift

Logical Right Shift

```php
public _base256_rshift(string& $x, int $shift): string
```

Shifts binary strings $shift bits, essentially dividing by 2**$shift and returning the remainder.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **string** | (by referenc) |
| `$shift` | **int** |  |





***

### _int2bytes

Converts 32-bit integers to bytes.

```php
public _int2bytes(int $x): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** |  |





***

### _bytes2int

Converts bytes to 32-bit integers

```php
public _bytes2int(string $x): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **string** |  |





***

### _encodeASN1Length

DER-encode an integer

```php
public _encodeASN1Length(int $length): string
```

The ability to DER-encode integers is needed to create RSA public keys for use with OpenSSL






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** |  |





**See Also:**

* \phpseclib\Math\self::modPow() - 

***

### _safe_divide

Single digit division

```php
public _safe_divide(int $x, int $y): int
```

Even if int64 is being used the division operator will return a float64 value
if the dividend is not evenly divisible by the divisor. Since a float64 doesn't
have the precision of int64 this is a problem so, when int64 is being used,
we'll guarantee that the dividend is divisible by first subtracting the remainder.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** |  |
| `$y` | **int** |  |





***


***
> Automatically generated on 2025-03-15
