***

# Blowfish

Pure-PHP implementation of Blowfish.



* Full name: `\phpseclib\Crypt\Blowfish`
* Parent class: [`\phpseclib\Crypt\Base`](./Base.md)



## Properties


### block_size

Block Length of the cipher

```php
public int $block_size
```





**See Also:**

* \phpseclib\Crypt\Base::block_size - 

***

### cipher_name_mcrypt

The mcrypt specific name of the cipher

```php
public string $cipher_name_mcrypt
```





**See Also:**

* \phpseclib\Crypt\Base::cipher_name_mcrypt - 

***

### cfb_init_len

Optimizing value while CFB-encrypting

```php
public int $cfb_init_len
```





**See Also:**

* \phpseclib\Crypt\Base::cfb_init_len - 

***

### sha512

SHA512 Object

```php
public object $sha512
```





**See Also:**

* \phpseclib\Crypt\self::bcrypt_pbkdf - 

***

### sbox0

The fixed subkeys boxes ($sbox0 - $sbox3) with 256 entries each

```php
public array $sbox0
```

S-Box 0




***

### sbox1

S-Box 1

```php
public array $sbox1
```






***

### sbox2

S-Box 2

```php
public array $sbox2
```






***

### sbox3

S-Box 3

```php
public array $sbox3
```






***

### parray

P-Array consists of 18 32-bit subkeys

```php
public array $parray
```






***

### bctx

The BCTX-working Array

```php
public array $bctx
```

Holds the expanded key [p] and the key-depended s-boxes [sb]




***

### kl

Holds the last used key

```php
public array $kl
```






***

## Methods


### __construct

Default Constructor.

```php
public __construct(int $mode = self::MODE_CBC): mixed
```

Determines whether or not the mcrypt extension should be used.

$mode could be:

- CRYPT_MODE_ECB

- CRYPT_MODE_CBC

- CRYPT_MODE_CTR

- CRYPT_MODE_CFB

- CRYPT_MODE_OFB

(or the alias constants of the chosen cipher, for example for AES: CRYPT_AES_MODE_ECB or CRYPT_AES_MODE_CBC ...)

If not explicitly set, CRYPT_MODE_CBC will be used.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** |  |





***

### setKeyLength

Sets the key length.

```php
public setKeyLength(int $length): mixed
```

Key lengths can be between 32 and 448 bits.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** |  |





***

### isValidEngine

Test for engine validity

```php
public isValidEngine(int $engine): bool
```

This is mainly just a wrapper to set things up for \phpseclib\Crypt\Base::isValidEngine()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$engine` | **int** |  |





**See Also:**

* \phpseclib\Crypt\Base::isValidEngine() - 

***

### _setupKey

Setup the key (expansion)

```php
public _setupKey(): mixed
```












**See Also:**

* \phpseclib\Crypt\Base::_setupKey() - 

***

### _bcrypt_hash

bcrypt

```php
public _bcrypt_hash(string $sha2pass, string $sha2salt): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sha2pass` | **string** |  |
| `$sha2salt` | **string** |  |





***

### bcrypt_pbkdf

Performs OpenSSH-style bcrypt

```php
public bcrypt_pbkdf(string $pass, string $salt, int $keylen, int $rounds): false|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pass` | **string** |  |
| `$salt` | **string** |  |
| `$keylen` | **int** |  |
| `$rounds` | **int** |  |





***

### _expand0state

Key expansion without salt

```php
public _expand0state(int[] $key, int[]& $sbox0, int[]& $sbox1, int[]& $sbox2, int[]& $sbox3, int[]& $p): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int[]** |  |
| `$sbox0` | **int[]** |  |
| `$sbox1` | **int[]** |  |
| `$sbox2` | **int[]** |  |
| `$sbox3` | **int[]** |  |
| `$p` | **int[]** |  |





**See Also:**

* \phpseclib\Crypt\self::_bcrypt_hash() - 

***

### _expandstate

Key expansion with salt

```php
public _expandstate(int[] $data, int[] $key, int[]& $sbox0, int[]& $sbox1, int[]& $sbox2, int[]& $sbox3, int[]& $p): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **int[]** |  |
| `$key` | **int[]** |  |
| `$sbox0` | **int[]** |  |
| `$sbox1` | **int[]** |  |
| `$sbox2` | **int[]** |  |
| `$sbox3` | **int[]** |  |
| `$p` | **int[]** |  |





**See Also:**

* \phpseclib\Crypt\self::_bcrypt_hash() - 

***

### _encryptBlock

Encrypts a block

```php
public _encryptBlock(string $in): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **string** |  |





***

### _encryptBlockHelperFast

Fast helper function for block encryption

```php
public _encryptBlockHelperFast(int $x0, int $x1, int[] $sbox0, int[] $sbox1, int[] $sbox2, int[] $sbox3, int[] $p): int[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x0` | **int** |  |
| `$x1` | **int** |  |
| `$sbox0` | **int[]** |  |
| `$sbox1` | **int[]** |  |
| `$sbox2` | **int[]** |  |
| `$sbox3` | **int[]** |  |
| `$p` | **int[]** |  |





***

### _encryptBlockHelperSlow

Slow helper function for block encryption

```php
public _encryptBlockHelperSlow(int $x0, int $x1, int[] $sbox0, int[] $sbox1, int[] $sbox2, int[] $sbox3, int[] $p): int[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x0` | **int** |  |
| `$x1` | **int** |  |
| `$sbox0` | **int[]** |  |
| `$sbox1` | **int[]** |  |
| `$sbox2` | **int[]** |  |
| `$sbox3` | **int[]** |  |
| `$p` | **int[]** |  |





***

### _decryptBlock

Decrypts a block

```php
public _decryptBlock(string $in): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **string** |  |





***

### _setupInlineCrypt

Setup the performance-optimized function for de/encrypt()

```php
public _setupInlineCrypt(): mixed
```












**See Also:**

* \phpseclib\Crypt\Base::_setupInlineCrypt() - 

***


## Inherited methods


### __construct

Default Constructor.

```php
public __construct(int $mode = self::MODE_CBC): mixed
```

Determines whether or not the mcrypt extension should be used.

$mode could be:

- self::MODE_ECB

- self::MODE_CBC

- self::MODE_CTR

- self::MODE_CFB

- self::MODE_OFB

If not explicitly set, self::MODE_CBC will be used.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** |  |





***

### setKeyLength

Sets the key length.

```php
public setKeyLength(int $length): mixed
```

Keys with explicitly set lengths need to be treated accordingly






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** |  |





***

### getKeyLength

Returns the current key length in bits

```php
public getKeyLength(): int
```












***

### getBlockLength

Returns the current block length in bits

```php
public getBlockLength(): int
```












***

### _openssl_ctr_process

OpenSSL CTR Processor

```php
public _openssl_ctr_process(string $plaintext, string& $encryptIV, array& $buffer): string
```

PHP's OpenSSL bindings do not operate in continuous mode so we'll wrap around it. Since the keystream
for CTR is the same for both encrypting and decrypting this function is re-used by both Base::encrypt()
and Base::decrypt(). Also, OpenSSL doesn't implement CTR for all of it's symmetric ciphers so this
function will emulate CTR with ECB when necessary.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plaintext` | **string** |  |
| `$encryptIV` | **string** |  |
| `$buffer` | **array** |  |





**See Also:**

* \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::decrypt() - 

***

### _openssl_ofb_process

OpenSSL OFB Processor

```php
public _openssl_ofb_process(string $plaintext, string& $encryptIV, array& $buffer): string
```

PHP's OpenSSL bindings do not operate in continuous mode so we'll wrap around it. Since the keystream
for OFB is the same for both encrypting and decrypting this function is re-used by both Base::encrypt()
and Base::decrypt().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plaintext` | **string** |  |
| `$encryptIV` | **string** |  |
| `$buffer` | **array** |  |





**See Also:**

* \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::decrypt() - 

***

### _openssl_translate_mode

phpseclib <-> OpenSSL Mode Mapper

```php
public _openssl_translate_mode(): int
```

May need to be overwritten by classes extending this one in some cases










***

### enablePadding

Pad "packets".

```php
public enablePadding(): mixed
```

Block ciphers working by encrypting between their specified [$this->]block_size at a time
If you ever need to encrypt or decrypt something that isn't of the proper length, it becomes necessary to
pad the input so that it is of the proper length.

Padding is enabled by default.  Sometimes, however, it is undesirable to pad strings.  Such is the case in SSH,
where "packets" are padded with random bytes before being encrypted.  Unpad these packets and you risk stripping
away characters that shouldn't be stripped away. (SSH knows how many bytes are added because the length is
transmitted separately)










**See Also:**

* \phpseclib\Crypt\self::disablePadding() - 

***

### disablePadding

Do not pad packets.

```php
public disablePadding(): mixed
```












**See Also:**

* \phpseclib\Crypt\self::enablePadding() - 

***

### isValidEngine

Test for engine validity

```php
public isValidEngine(int $engine): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$engine` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::__construct() - 

***

### setPreferredEngine

Sets the preferred crypt engine

```php
public setPreferredEngine(int $engine): mixed
```

Currently, $engine could be:

- \phpseclib\Crypt\Base::ENGINE_OPENSSL  [very fast]

- \phpseclib\Crypt\Base::ENGINE_MCRYPT   [fast]

- \phpseclib\Crypt\Base::ENGINE_INTERNAL [slow]

If the preferred crypt engine is not available the fastest available one will be used






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$engine` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::__construct() - 

***

### getEngine

Returns the engine currently being utilized

```php
public getEngine(): mixed
```












**See Also:**

* \phpseclib\Crypt\self::_setEngine() - 

***

### _setEngine

Sets the engine as appropriate

```php
public _setEngine(): mixed
```












**See Also:**

* \phpseclib\Crypt\self::__construct() - 

***

### _encryptBlock

Encrypts a block

```php
public _encryptBlock(string $in): string
```

Note: Must be extended by the child \phpseclib\Crypt\* class


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **string** |  |





***

### _decryptBlock

Decrypts a block

```php
public _decryptBlock(string $in): string
```

Note: Must be extended by the child \phpseclib\Crypt\* class


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **string** |  |





***

### _setupKey

Setup the key (expansion)

```php
public _setupKey(): mixed
```

Only used if $engine == self::ENGINE_INTERNAL

Note: Must extend by the child \phpseclib\Crypt\* class


* This method is **abstract**.







**See Also:**

* \phpseclib\Crypt\self::_setup() - 

***

### _pad

Pads a string

```php
public _pad(string $text): string
```

Pads a string using the RSA PKCS padding standards so that its length is a multiple of the blocksize.
$this->block_size - (strlen($text) % $this->block_size) bytes are added, each of which is equal to
chr($this->block_size - (strlen($text) % $this->block_size)

If padding is disabled and $text is not a multiple of the blocksize, the string will be padded regardless
and padding will, hence forth, be enabled.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::_unpad() - 

***

### _unpad

Unpads a string.

```php
public _unpad(string $text): string
```

If padding is enabled and the reported padding length is invalid the encryption key will be assumed to be wrong
and false will be returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::_pad() - 

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

### _string_pop

String Pop

```php
public _string_pop(string& $string, int $index = 1): string
```

Inspired by array_pop






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$index` | **int** |  |





***

### _increment_str

Increment the current string

```php
public _increment_str(string& $var): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::decrypt() - * \phpseclib\Crypt\self::encrypt() - 

***

### _createInlineCryptFunction

Creates the performance-optimized function for en/decrypt()

```php
public _createInlineCryptFunction(array $cipher_code): string
```

Internally for phpseclib developers:

_createInlineCryptFunction():

- merge the $cipher_code [setup'ed by _setupInlineCrypt()]
  with the current [$this->]mode of operation code

- create the $inline function, which called by encrypt() / decrypt()
  as its replacement to speed up the en/decryption operations.

- return the name of the created $inline callback function

- used to speed up en/decryption



The main reason why can speed up things [up to 50%] this way are:

- using variables more effective then regular.
  (ie no use of expensive arrays but integers $k_0, $k_1 ...
  or even, for example, the pure $key[] values hardcoded)

- avoiding 1000's of function calls of ie _encryptBlock()
  but inlining the crypt operations.
  in the mode of operation for() loop.

- full loop unroll the (sometimes key-dependent) rounds
  avoiding this way ++$i counters and runtime-if's etc...

The basic code architectur of the generated $inline en/decrypt()
lambda function, in pseudo php, is:

<code>
+----------------------------------------------------------------------------------------------+
| callback $inline = create_function:                                                          |
| lambda_function_0001_crypt_ECB($action, $text)                                               |
| {                                                                                            |
|     INSERT PHP CODE OF:                                                                      |
|     $cipher_code['init_crypt'];                  // general init code.                       |
|                                                  // ie: $sbox'es declarations used for       |
|                                                  //     encrypt and decrypt'ing.             |
|                                                                                              |
|     switch ($action) {                                                                       |
|         case 'encrypt':                                                                      |
|             INSERT PHP CODE OF:                                                              |
|             $cipher_code['init_encrypt'];       // encrypt sepcific init code.               |
|                                                    ie: specified $key or $box                |
|                                                        declarations for encrypt'ing.         |
|                                                                                              |
|             foreach ($ciphertext) {                                                          |
|                 $in = $block_size of $ciphertext;                                            |
|                                                                                              |
|                 INSERT PHP CODE OF:                                                          |
|                 $cipher_code['encrypt_block'];  // encrypt's (string) $in, which is always:  |
|                                                 // strlen($in) == $this->block_size          |
|                                                 // here comes the cipher algorithm in action |
|                                                 // for encryption.                           |
|                                                 // $cipher_code['encrypt_block'] has to      |
|                                                 // encrypt the content of the $in variable   |
|                                                                                              |
|                 $plaintext .= $in;                                                           |
|             }                                                                                |
|             return $plaintext;                                                               |
|                                                                                              |
|         case 'decrypt':                                                                      |
|             INSERT PHP CODE OF:                                                              |
|             $cipher_code['init_decrypt'];       // decrypt sepcific init code                |
|                                                    ie: specified $key or $box                |
|                                                        declarations for decrypt'ing.         |
|             foreach ($plaintext) {                                                           |
|                 $in = $block_size of $plaintext;                                             |
|                                                                                              |
|                 INSERT PHP CODE OF:                                                          |
|                 $cipher_code['decrypt_block'];  // decrypt's (string) $in, which is always   |
|                                                 // strlen($in) == $this->block_size          |
|                                                 // here comes the cipher algorithm in action |
|                                                 // for decryption.                           |
|                                                 // $cipher_code['decrypt_block'] has to      |
|                                                 // decrypt the content of the $in variable   |
|                 $ciphertext .= $in;                                                          |
|             }                                                                                |
|             return $ciphertext;                                                              |
|     }                                                                                        |
| }                                                                                            |
+----------------------------------------------------------------------------------------------+
</code>

See also the \phpseclib\Crypt\*::_setupInlineCrypt()'s for
productive inline $cipher_code's how they works.

Structure of:
<code>
$cipher_code = array(
    'init_crypt'    => (string) '', // optional
    'init_encrypt'  => (string) '', // optional
    'init_decrypt'  => (string) '', // optional
    'encrypt_block' => (string) '', // required
    'decrypt_block' => (string) ''  // required
);
</code>






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cipher_code` | **array** |  |


**Return Value:**

(the name of the created callback function)




**See Also:**

* \phpseclib\Crypt\self::_setupInlineCrypt() - * \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::decrypt() - 

***

### _getLambdaFunctions

Holds the lambda_functions table (classwide)

```php
public _getLambdaFunctions(): array
```

Each name of the lambda function, created from
_setupInlineCrypt() && _createInlineCryptFunction()
is stored, classwide (!), here for reusing.

The string-based index of $function is a classwide
unique value representing, at least, the $mode of
operation (or more... depends of the optimizing level)
for which $mode the lambda function was created.







**Return Value:**

&$functions




***

### _hashInlineCryptFunction

Generates a digest from $bytes

```php
public _hashInlineCryptFunction(string $bytes): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::_setupInlineCrypt() - 

***

### safe_intval

Convert float to int

```php
public safe_intval(string $x): int
```

On ARM CPUs converting floats to ints doesn't always work






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **string** |  |





***

### safe_intval_inline

eval()'able string for in-line float to int

```php
public safe_intval_inline(): string
```












***

### do_nothing

Dummy error handler to suppress mcrypt errors

```php
public do_nothing(): mixed
```












***

### continuousBufferEnabled

Is the continuous buffer enabled?

```php
public continuousBufferEnabled(): bool
```












***


***
> Automatically generated on 2025-03-15
