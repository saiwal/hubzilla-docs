***

# Base

Base Class for all \phpseclib\Crypt\* cipher classes



* Full name: `\phpseclib\Crypt\Base`
* This class is an **Abstract class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`MODE_CTR`|public| |-1|
|`MODE_ECB`|public| |1|
|`MODE_CBC`|public| |2|
|`MODE_CFB`|public| |3|
|`MODE_CFB8`|public| |6|
|`MODE_OFB8`|public| |7|
|`MODE_OFB`|public| |4|
|`MODE_STREAM`|public| |5|
|`ENGINE_INTERNAL`|public| |1|
|`ENGINE_MCRYPT`|public| |2|
|`ENGINE_OPENSSL`|public| |3|

## Properties


### WHIRLPOOL_AVAILABLE

Whirlpool available flag

```php
public static bool $WHIRLPOOL_AVAILABLE
```



* This property is **static**.

**See Also:**

* \phpseclib\Crypt\Base::_hashInlineCryptFunction() - 

***

### mode

The Encryption Mode

```php
public int $mode
```





**See Also:**

* \phpseclib\Crypt\self::__construct() - 

***

### block_size

The Block Length of the block cipher

```php
public int $block_size
```






***

### key

The Key

```php
public string $key
```





**See Also:**

* \phpseclib\Crypt\self::setKey() - 

***

### iv

The Initialization Vector

```php
public string $iv
```





**See Also:**

* \phpseclib\Crypt\self::setIV() - 

***

### encryptIV

A "sliding" Initialization Vector

```php
public string $encryptIV
```





**See Also:**

* \phpseclib\Crypt\self::enableContinuousBuffer() - * \phpseclib\Crypt\self::_clearBuffers() - 

***

### decryptIV

A "sliding" Initialization Vector

```php
public string $decryptIV
```





**See Also:**

* \phpseclib\Crypt\self::enableContinuousBuffer() - * \phpseclib\Crypt\self::_clearBuffers() - 

***

### continuousBuffer

Continuous Buffer status

```php
public bool $continuousBuffer
```





**See Also:**

* \phpseclib\Crypt\self::enableContinuousBuffer() - 

***

### enbuffer

Encryption buffer for CTR, OFB and CFB modes

```php
public array $enbuffer
```





**See Also:**

* \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::_clearBuffers() - 

***

### debuffer

Decryption buffer for CTR, OFB and CFB modes

```php
public array $debuffer
```





**See Also:**

* \phpseclib\Crypt\self::decrypt() - * \phpseclib\Crypt\self::_clearBuffers() - 

***

### enmcrypt

mcrypt resource for encryption

```php
public resource $enmcrypt
```

The mcrypt resource can be recreated every time something needs to be created or it can be created just once.
Since mcrypt operates in continuous mode, by default, it'll need to be recreated when in non-continuous mode.



**See Also:**

* \phpseclib\Crypt\self::encrypt() - 

***

### demcrypt

mcrypt resource for decryption

```php
public resource $demcrypt
```

The mcrypt resource can be recreated every time something needs to be created or it can be created just once.
Since mcrypt operates in continuous mode, by default, it'll need to be recreated when in non-continuous mode.



**See Also:**

* \phpseclib\Crypt\self::decrypt() - 

***

### enchanged

Does the enmcrypt resource need to be (re)initialized?

```php
public bool $enchanged
```





**See Also:**

* \phpseclib\Crypt\Twofish::setKey() - * \phpseclib\Crypt\Twofish::setIV() - 

***

### dechanged

Does the demcrypt resource need to be (re)initialized?

```php
public bool $dechanged
```





**See Also:**

* \phpseclib\Crypt\Twofish::setKey() - * \phpseclib\Crypt\Twofish::setIV() - 

***

### ecb

mcrypt resource for CFB mode

```php
public resource $ecb
```

mcrypt's CFB mode, in (and only in) buffered context,
is broken, so phpseclib implements the CFB mode by it self,
even when the mcrypt php extension is available.

In order to do the CFB-mode work (fast) phpseclib
use a separate ECB-mode mcrypt resource.



**See Also:**

* \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::decrypt() - * \phpseclib\Crypt\self::_setupMcrypt() - * http://phpseclib.sourceforge.net/cfb-demo.phps - 

***

### cfb_init_len

Optimizing value while CFB-encrypting

```php
public int $cfb_init_len
```

Only relevant if $continuousBuffer enabled
and $engine == self::ENGINE_MCRYPT

It's faster to re-init $enmcrypt if
$buffer bytes > $cfb_init_len than
using the $ecb resource furthermore.

This value depends of the chosen cipher
and the time it would be needed for it's
initialization [by mcrypt_generic_init()]
which, typically, depends on the complexity
on its internaly Key-expanding algorithm.



**See Also:**

* \phpseclib\Crypt\self::encrypt() - 

***

### changed

Does internal cipher state need to be (re)initialized?

```php
public bool $changed
```





**See Also:**

* \phpseclib\Crypt\self::setKey() - * \phpseclib\Crypt\self::setIV() - * \phpseclib\Crypt\self::disableContinuousBuffer() - 

***

### padding

Padding status

```php
public bool $padding
```





**See Also:**

* \phpseclib\Crypt\self::enablePadding() - 

***

### paddable

Is the mode one that is paddable?

```php
public bool $paddable
```





**See Also:**

* \phpseclib\Crypt\self::__construct() - 

***

### engine

Holds which crypt engine internaly should be use,
which will be determined automatically on __construct()

```php
public int $engine
```

Currently available $engines are:
- self::ENGINE_OPENSSL  (very fast, php-extension: openssl, extension_loaded('openssl') required)
- self::ENGINE_MCRYPT   (fast, php-extension: mcrypt, extension_loaded('mcrypt') required)
- self::ENGINE_INTERNAL (slower, pure php-engine, no php-extension required)



**See Also:**

* \phpseclib\Crypt\self::_setEngine() - * \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::decrypt() - 

***

### preferredEngine

Holds the preferred crypt engine

```php
public int $preferredEngine
```





**See Also:**

* \phpseclib\Crypt\self::_setEngine() - * \phpseclib\Crypt\self::setPreferredEngine() - 

***

### cipher_name_mcrypt

The mcrypt specific name of the cipher

```php
public string $cipher_name_mcrypt
```

Only used if $engine == self::ENGINE_MCRYPT



**See Also:**

* \phpseclib\Crypt\self::_setupMcrypt() - * http://www.php.net/mcrypt_module_open - * http://www.php.net/mcrypt_list_algorithms - 

***

### cipher_name_openssl

The openssl specific name of the cipher

```php
public string $cipher_name_openssl
```

Only used if $engine == self::ENGINE_OPENSSL



**See Also:**

* http://www.php.net/openssl-get-cipher-methods - 

***

### cipher_name_openssl_ecb

The openssl specific name of the cipher in ECB mode

```php
public string $cipher_name_openssl_ecb
```

If OpenSSL does not support the mode we're trying to use (CTR)
it can still be emulated with ECB mode.



**See Also:**

* http://www.php.net/openssl-get-cipher-methods - 

***

### password_default_salt

The default salt used by setPassword()

```php
public string $password_default_salt
```





**See Also:**

* \phpseclib\Crypt\self::setPassword() - 

***

### inline_crypt

The name of the performance-optimized callback function

```php
public callable $inline_crypt
```

Used by encrypt() / decrypt()
only if $engine == self::ENGINE_INTERNAL



**See Also:**

* \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::decrypt() - * \phpseclib\Crypt\self::_setupInlineCrypt() - * \phpseclib\Crypt\self::$use_inline_crypt - 

***

### use_inline_crypt

Holds whether performance-optimized $inline_crypt() can/should be used.

```php
public mixed $use_inline_crypt
```





**See Also:**

* \phpseclib\Crypt\self::encrypt() - * \phpseclib\Crypt\self::decrypt() - * \phpseclib\Crypt\self::inline_crypt - 

***

### openssl_emulate_ctr

If OpenSSL can be used in ECB but not in CTR we can emulate CTR

```php
public bool $openssl_emulate_ctr
```





**See Also:**

* \phpseclib\Crypt\self::_openssl_ctr_process() - 

***

### openssl_options

Determines what options are passed to openssl_encrypt/decrypt

```php
public mixed $openssl_options
```





**See Also:**

* \phpseclib\Crypt\self::isValidEngine() - 

***

### explicit_key_length

Has the key length explicitly been set or should it be derived from the key, itself?

```php
public bool $explicit_key_length
```





**See Also:**

* \phpseclib\Crypt\self::setKeyLength() - 

***

### skip_key_adjustment

Don't truncate / null pad key

```php
public bool $skip_key_adjustment
```





**See Also:**

* \phpseclib\Crypt\self::_clearBuffers() - 

***

## Methods


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
