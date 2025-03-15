
# Hash

Pure-PHP implementations of keyed-hash message authentication codes (HMACs) and various cryptographic hashing functions.



* Full name: `\phpseclib\Crypt\Hash`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`MODE_INTERNAL`|public| |1|
|`MODE_MHASH`|public| |2|
|`MODE_HASH`|public| |3|

## Properties


### hashParam

Hash Parameter

```php
public int $hashParam
```





**See Also:**

* \phpseclib\Crypt\self::setHash() - 

***

### b

Byte-length of compression blocks / key (Internal HMAC)

```php
public int $b
```





**See Also:**

* \phpseclib\Crypt\self::setAlgorithm() - 

***

### l

Byte-length of hash output (Internal HMAC)

```php
public int $l
```





**See Also:**

* \phpseclib\Crypt\self::setHash() - 

***

### hash

Hash Algorithm

```php
public string $hash
```





**See Also:**

* \phpseclib\Crypt\self::setHash() - 

***

### key

Key

```php
public string $key
```





**See Also:**

* \phpseclib\Crypt\self::setKey() - 

***

### computedKey

Computed Key

```php
public string $computedKey
```





**See Also:**

* \phpseclib\Crypt\self::_computeKey() - 

***

### opad

Outer XOR (Internal HMAC)

```php
public string $opad
```





**See Also:**

* \phpseclib\Crypt\self::setKey() - 

***

### ipad

Inner XOR (Internal HMAC)

```php
public string $ipad
```





**See Also:**

* \phpseclib\Crypt\self::setKey() - 

***

### engine

Engine

```php
public string $engine
```





**See Also:**

* \phpseclib\Crypt\self::setHash() - 

***

## Methods


### __construct

Default Constructor.

```php
public __construct(string $hash = &#039;sha1&#039;): \phpseclib\Crypt\Hash
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** |  |





***

### setKey

Sets the key for HMACs

```php
public setKey(string $key = false): mixed
```

Keys can be of any length.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |





***

### _computeKey

Pre-compute the key used by the HMAC

```php
public _computeKey(): mixed
```

Quoting http://tools.ietf.org/html/rfc2104#section-2, "Applications that use keys longer than B bytes
will first hash the key using H and then use the resultant L byte string as the actual key to HMAC."

As documented in https://www.reddit.com/r/PHP/comments/9nct2l/symfonypolyfill_hash_pbkdf2_correct_fix_for/
when doing an HMAC multiple times it's faster to compute the hash once instead of computing it during
every call










***

### getHash

Gets the hash function.

```php
public getHash(): string
```

As set by the constructor or by the setHash() method.










***

### setHash

Sets the hash function.

```php
public setHash(string $hash): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** |  |





***

### hash

Compute the HMAC.

```php
public hash(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### getLength

Returns the hash length (in bytes)

```php
public getLength(): int
```












***

### _md5

Wrapper for MD5

```php
public _md5(string $m): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _sha1

Wrapper for SHA1

```php
public _sha1(string $m): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _md2

Pure-PHP implementation of MD2

```php
public _md2(string $m): mixed
```

See {@link http://tools.ietf.org/html/rfc1319}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _sha256

Pure-PHP implementation of SHA256

```php
public _sha256(string $m): mixed
```

See {@link http://en.wikipedia.org/wiki/SHA_hash_functions#SHA-256_.28a_SHA-2_variant.29_pseudocode}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _sha512

Pure-PHP implementation of SHA384 and SHA512

```php
public _sha512(string $m): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _rightRotate

Right Rotate

```php
public _rightRotate(int $int, int $amt): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$int` | **int** |  |
| `$amt` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::_sha256() - 

***

### _rightShift

Right Shift

```php
public _rightShift(int $int, int $amt): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$int` | **int** |  |
| `$amt` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::_sha256() - 

***

### _not

Not

```php
public _not(int $int): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$int` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::_sha256() - 

***

### _add

Add

```php
public _add(): int
```

_sha256() adds multiple unsigned 32-bit integers.  Since PHP doesn't support unsigned integers and since the
possibility of overflow exists, care has to be taken.  BigInteger could be used but this should be faster.










**See Also:**

* \phpseclib\Crypt\self::_sha256() - 

***

### _string_shift

String Shift

```php
public _string_shift(string& $string, int $index = 1): string
```

Inspired by array_shift






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$index` | **int** |  |





***


***
> Automatically generated on 2025-03-15
