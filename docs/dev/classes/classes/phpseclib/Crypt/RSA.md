
# RSA

Pure-PHP PKCS#1 compliant implementation of RSA.



* Full name: `\phpseclib\Crypt\RSA`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`ENCRYPTION_OAEP`|public| |1|
|`ENCRYPTION_PKCS1`|public| |2|
|`ENCRYPTION_NONE`|public| |3|
|`SIGNATURE_PSS`|public| |1|
|`SIGNATURE_PKCS1`|public| |2|
|`ASN1_INTEGER`|public| |2|
|`ASN1_BITSTRING`|public| |3|
|`ASN1_OCTETSTRING`|public| |4|
|`ASN1_OBJECT`|public| |6|
|`ASN1_SEQUENCE`|public| |48|
|`MODE_INTERNAL`|public| |1|
|`MODE_OPENSSL`|public| |2|
|`PRIVATE_FORMAT_PKCS1`|public| |0|
|`PRIVATE_FORMAT_PUTTY`|public| |1|
|`PRIVATE_FORMAT_XML`|public| |2|
|`PRIVATE_FORMAT_PKCS8`|public| |8|
|`PRIVATE_FORMAT_OPENSSH`|public| |9|
|`PUBLIC_FORMAT_RAW`|public| |3|
|`PUBLIC_FORMAT_PKCS1`|public| |4|
|`PUBLIC_FORMAT_PKCS1_RAW`|public| |4|
|`PUBLIC_FORMAT_XML`|public| |5|
|`PUBLIC_FORMAT_OPENSSH`|public| |6|
|`PUBLIC_FORMAT_PKCS8`|public| |7|

## Properties


### zero

Precomputed Zero

```php
public \phpseclib\Math\BigInteger $zero
```






***

### one

Precomputed One

```php
public \phpseclib\Math\BigInteger $one
```






***

### privateKeyFormat

Private Key Format

```php
public int $privateKeyFormat
```






***

### publicKeyFormat

Public Key Format

```php
public int $publicKeyFormat
```






***

### modulus

Modulus (ie. n)

```php
public \phpseclib\Math\BigInteger $modulus
```






***

### k

Modulus length

```php
public \phpseclib\Math\BigInteger $k
```






***

### exponent

Exponent (ie. e or d)

```php
public \phpseclib\Math\BigInteger $exponent
```






***

### primes

Primes for Chinese Remainder Theorem (ie. p and q)

```php
public array $primes
```






***

### exponents

Exponents for Chinese Remainder Theorem (ie. dP and dQ)

```php
public array $exponents
```






***

### coefficients

Coefficients for Chinese Remainder Theorem (ie. qInv)

```php
public array $coefficients
```






***

### hashName

Hash name

```php
public string $hashName
```






***

### hash

Hash function

```php
public \phpseclib\Crypt\Hash $hash
```






***

### hLen

Length of hash function output

```php
public int $hLen
```






***

### sLen

Length of salt

```php
public int $sLen
```






***

### mgfHash

Hash function for the Mask Generation Function

```php
public \phpseclib\Crypt\Hash $mgfHash
```






***

### mgfHLen

Length of MGF hash function output

```php
public int $mgfHLen
```






***

### encryptionMode

Encryption mode

```php
public int $encryptionMode
```






***

### signatureMode

Signature mode

```php
public int $signatureMode
```






***

### publicExponent

Public Exponent

```php
public mixed $publicExponent
```






***

### password

Password

```php
public string $password
```






***

### components

Components

```php
public array $components
```

For use with parsing XML formatted keys.  PHP's XML Parser functions use utilized - instead of PHP's DOM functions -
because PHP's XML Parser functions work on PHP4 whereas PHP's DOM functions - although surperior - don't.



**See Also:**

* \phpseclib\Crypt\self::_start_element_handler() - 

***

### current

Current String

```php
public mixed $current
```

For use with parsing XML formatted keys.



**See Also:**

* \phpseclib\Crypt\self::_character_handler() - * \phpseclib\Crypt\self::_stop_element_handler() - 

***

### configFile

OpenSSL configuration file name.

```php
public mixed $configFile
```

Set to null to use system configuration file.



**See Also:**

* \phpseclib\Crypt\self::createKey() - 

***

### comment

Public key comment field.

```php
public string $comment
```






***

## Methods


### __construct

The constructor

```php
public __construct(): \phpseclib\Crypt\RSA
```

If you want to make use of the openssl extension, you'll need to set the mode manually, yourself.  The reason
\phpseclib\Crypt\RSA doesn't do it is because OpenSSL doesn't fail gracefully.  openssl_pkey_new(), in particular, requires
openssl.cnf be present somewhere and, unfortunately, the only real way to find out is too late.










***

### createKey

Create public / private key pair

```php
public createKey(int $bits = 1024, int $timeout = false, array $partial = array()): mixed
```

Returns an array with the following three elements:
- 'privatekey': The private key.
- 'publickey':  The public key.
- 'partialkey': A partially computed key (if the execution time exceeded $timeout).
                Will need to be passed back to \phpseclib\Crypt\RSA::createKey() as the third parameter for further processing.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bits` | **int** |  |
| `$timeout` | **int** |  |
| `$partial` | **array** |  |





***

### _convertPrivateKey

Convert a private key to the appropriate format.

```php
public _convertPrivateKey(\phpseclib\Crypt\Math_BigInteger $n, \phpseclib\Crypt\Math_BigInteger $e, \phpseclib\Crypt\Math_BigInteger $d, array&lt;int,\phpseclib\Crypt\Math_BigInteger&gt; $primes, array&lt;int,\phpseclib\Crypt\Math_BigInteger&gt; $exponents, array&lt;int,\phpseclib\Crypt\Math_BigInteger&gt; $coefficients): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **\phpseclib\Crypt\Math_BigInteger** |  |
| `$e` | **\phpseclib\Crypt\Math_BigInteger** |  |
| `$d` | **\phpseclib\Crypt\Math_BigInteger** |  |
| `$primes` | **array<int,\phpseclib\Crypt\Math_BigInteger>** |  |
| `$exponents` | **array<int,\phpseclib\Crypt\Math_BigInteger>** |  |
| `$coefficients` | **array<int,\phpseclib\Crypt\Math_BigInteger>** |  |





**See Also:**

* \phpseclib\Crypt\self::setPrivateKeyFormat() - 

***

### _convertPublicKey

Convert a public key to the appropriate format

```php
public _convertPublicKey(\phpseclib\Crypt\Math_BigInteger $n, \phpseclib\Crypt\Math_BigInteger $e): string|array&lt;string,\phpseclib\Crypt\Math_BigInteger&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **\phpseclib\Crypt\Math_BigInteger** |  |
| `$e` | **\phpseclib\Crypt\Math_BigInteger** |  |





**See Also:**

* \phpseclib\Crypt\self::setPublicKeyFormat() - 

***

### _parseKey

Break a public or private key down into its constituant components

```php
public _parseKey(string|array $key, int $type): array|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string&#124;array** |  |
| `$type` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::_convertPublicKey() - * \phpseclib\Crypt\self::_convertPrivateKey() - 

***

### getSize

Returns the key size

```php
public getSize(): int
```

More specifically, this returns the size of the modulo in bits.










***

### _start_element_handler

Start Element Handler

```php
public _start_element_handler(resource $parser, string $name, array $attribs): mixed
```

Called by xml_set_element_handler()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parser` | **resource** |  |
| `$name` | **string** |  |
| `$attribs` | **array** |  |





***

### _stop_element_handler

Stop Element Handler

```php
public _stop_element_handler(resource $parser, string $name): mixed
```

Called by xml_set_element_handler()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parser` | **resource** |  |
| `$name` | **string** |  |





***

### _data_handler

Data Handler

```php
public _data_handler(resource $parser, string $data): mixed
```

Called by xml_set_character_data_handler()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parser` | **resource** |  |
| `$data` | **string** |  |





***

### loadKey

Loads a public or private key

```php
public loadKey(string|\phpseclib\Crypt\RSA|array $key, bool|int $type = false): bool
```

Returns true on success and false on failure (ie. an incorrect password was provided or the key was malformed)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string&#124;\phpseclib\Crypt\RSA&#124;array** |  |
| `$type` | **bool&#124;int** | optional |





***

### setPassword

Sets the password

```php
public setPassword(string $password = false): mixed
```

Private keys can be encrypted with a password.  To unset the password, pass in the empty string or false.
Or rather, pass in $password such that empty($password) && !is_string($password) is true.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$password` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::createKey() - * \phpseclib\Crypt\self::loadKey() - 

***

### setPublicKey

Defines the public key

```php
public setPublicKey(string $key = false, int $type = false): bool
```

Some private key formats define the public exponent and some don't.  Those that don't define it are problematic when
used in certain contexts.  For example, in SSH-2, RSA authentication works by sending the public key along with a
message signed by the private key to the server.  The SSH-2 server looks the public key up in an index of public keys
and if it's present then proceeds to verify the signature.  Problem is, if your private key doesn't include the public
exponent this won't work unless you manually add the public exponent. phpseclib tries to guess if the key being used
is the public key but in the event that it guesses incorrectly you might still want to explicitly set the key as being
public.

Do note that when a new key is loaded the index will be cleared.

Returns true on success, false on failure






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | optional |
| `$type` | **int** | optional |





**See Also:**

* \phpseclib\Crypt\self::getPublicKey() - 

***

### setPrivateKey

Defines the private key

```php
public setPrivateKey(string $key = false, int $type = false): bool
```

If phpseclib guessed a private key was a public key and loaded it as such it might be desirable to force
phpseclib to treat the key as a private key. This function will do that.

Do note that when a new key is loaded the index will be cleared.

Returns true on success, false on failure






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | optional |
| `$type` | **int** | optional |





**See Also:**

* \phpseclib\Crypt\self::getPublicKey() - 

***

### getPublicKey

Returns the public key

```php
public getPublicKey(int $type = self::PUBLIC_FORMAT_PKCS8): mixed
```

The public key is only returned under two circumstances - if the private key had the public key embedded within it
or if the public key was set via setPublicKey().  If the currently loaded key is supposed to be the public key this
function won't return it since this library, for the most part, doesn't distinguish between public and private keys.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** | optional |





**See Also:**

* \phpseclib\Crypt\self::getPublicKey() - 

***

### getPublicKeyFingerprint

Returns the public key's fingerprint

```php
public getPublicKeyFingerprint(string $algorithm = &#039;md5&#039;): mixed
```

The public key's fingerprint is returned, which is equivalent to running `ssh-keygen -lf rsa.pub`. If there is
no public key currently loaded, false is returned.
Example output (md5): "c1:b1:30:29:d7:b8:de:6c:97:77:10:d7:46:41:63:87" (as specified by RFC 4716)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$algorithm` | **string** | The hashing algorithm to be used. Valid options are &#039;md5&#039; and &#039;sha256&#039;. False is returned<br />for invalid values. |





***

### getPrivateKey

Returns the private key

```php
public getPrivateKey(int $type = self::PUBLIC_FORMAT_PKCS1): mixed
```

The private key is only returned if the currently loaded key contains the constituent prime numbers.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** | optional |





**See Also:**

* \phpseclib\Crypt\self::getPublicKey() - 

***

### _getPrivatePublicKey

Returns a minimalistic private key

```php
public _getPrivatePublicKey(int $mode = self::PUBLIC_FORMAT_PKCS8): mixed
```

Returns the private key without the prime number constituants.  Structurally identical to a public key that
hasn't been set as the public key






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** | optional |





**See Also:**

* \phpseclib\Crypt\self::getPrivateKey() - 

***

### __toString

__toString() magic method

```php
public __toString(): string
```












***

### __clone

__clone() magic method

```php
public __clone(): \phpseclib\Crypt\Crypt_RSA
```












***

### _generateMinMax

Generates the smallest and largest numbers requiring $bits bits

```php
public _generateMinMax(int $bits): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bits` | **int** |  |





***

### _decodeLength

DER-decode the length

```php
public _decodeLength(string& $string): int
```

DER supports lengths up to (2**8)**127, however, we'll only support lengths up to (2**8)**4.  See
{@link http://itu.int/ITU-T/studygroups/com17/languages/X.690-0207.pdf#p=13} for more information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |





***

### _encodeLength

DER-encode the length

```php
public _encodeLength(int $length): string
```

DER supports lengths up to (2**8)**127, however, we'll only support lengths up to (2**8)**4.  See
{@link http://itu.int/ITU-T/studygroups/com17/languages/X.690-0207.pdf#p=13} for more information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** |  |





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

### setPrivateKeyFormat

Determines the private key format

```php
public setPrivateKeyFormat(int $format): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::createKey() - 

***

### setPublicKeyFormat

Determines the public key format

```php
public setPublicKeyFormat(int $format): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **int** |  |





**See Also:**

* \phpseclib\Crypt\self::createKey() - 

***

### setHash

Determines which hashing function should be used

```php
public setHash(string $hash): mixed
```

Used with signature production / verification and (if the encryption mode is self::ENCRYPTION_OAEP) encryption and
decryption.  If $hash isn't supported, sha1 is used.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** |  |





***

### setMGFHash

Determines which hashing function should be used for the mask generation function

```php
public setMGFHash(string $hash): mixed
```

The mask generation function is used by self::ENCRYPTION_OAEP and self::SIGNATURE_PSS and although it's
best if Hash and MGFHash are set to the same thing this is not a requirement.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** |  |





***

### setSaltLength

Determines the salt length

```php
public setSaltLength(int $sLen): mixed
```

To quote from {@link http://tools.ietf.org/html/rfc3447#page-38}:

Typical salt lengths in octets are hLen (the length of the output
of the hash function Hash) and 0.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sLen` | **int** |  |





***

### _i2osp

Integer-to-Octet-String primitive

```php
public _i2osp(\phpseclib\Math\BigInteger $x, int $xLen): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-4.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **\phpseclib\Math\BigInteger** |  |
| `$xLen` | **int** |  |





***

### _os2ip

Octet-String-to-Integer primitive

```php
public _os2ip(int|string|resource $x): \phpseclib\Math\BigInteger
```

See {@link http://tools.ietf.org/html/rfc3447#section-4.2}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int&#124;string&#124;resource** |  |





***

### _exponentiate

Exponentiate with or without Chinese Remainder Theorem

```php
public _exponentiate(\phpseclib\Math\BigInteger $x): \phpseclib\Math\BigInteger
```

See {@link http://tools.ietf.org/html/rfc3447#section-5.1.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **\phpseclib\Math\BigInteger** |  |





***

### _blind

Performs RSA Blinding

```php
public _blind(\phpseclib\Math\BigInteger $x, \phpseclib\Math\BigInteger $r, int $i): \phpseclib\Math\BigInteger
```

Protects against timing attacks by employing RSA Blinding.
Returns $x->modPow($this->exponents[$i], $this->primes[$i])






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **\phpseclib\Math\BigInteger** |  |
| `$r` | **\phpseclib\Math\BigInteger** |  |
| `$i` | **int** |  |





***

### _equals

Performs blinded RSA equality testing

```php
public _equals(string $x, string $y): bool
```

Protects against a particular type of timing attack described.

See {@link http://codahale.com/a-lesson-in-timing-attacks/}

Thanks for the heads up singpolyma!






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **string** |  |
| `$y` | **string** |  |





***

### _rsaep

RSAEP

```php
public _rsaep(\phpseclib\Math\BigInteger $m): \phpseclib\Math\BigInteger
```

See {@link http://tools.ietf.org/html/rfc3447#section-5.1.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **\phpseclib\Math\BigInteger** |  |





***

### _rsadp

RSADP

```php
public _rsadp(\phpseclib\Math\BigInteger $c): \phpseclib\Math\BigInteger
```

See {@link http://tools.ietf.org/html/rfc3447#section-5.1.2}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$c` | **\phpseclib\Math\BigInteger** |  |





***

### _rsasp1

RSASP1

```php
public _rsasp1(\phpseclib\Math\BigInteger $m): \phpseclib\Math\BigInteger
```

See {@link http://tools.ietf.org/html/rfc3447#section-5.2.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **\phpseclib\Math\BigInteger** |  |





***

### _rsavp1

RSAVP1

```php
public _rsavp1(\phpseclib\Math\BigInteger $s): \phpseclib\Math\BigInteger
```

See {@link http://tools.ietf.org/html/rfc3447#section-5.2.2}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **\phpseclib\Math\BigInteger** |  |





***

### _mgf1

MGF1

```php
public _mgf1(string $mgfSeed, int $maskLen): string
```

See {@link http://tools.ietf.org/html/rfc3447#appendix-B.2.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mgfSeed` | **string** |  |
| `$maskLen` | **int** |  |





***

### _rsaes_oaep_encrypt

RSAES-OAEP-ENCRYPT

```php
public _rsaes_oaep_encrypt(string $m, string $l = &#039;&#039;): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-7.1.1} and
{http://en.wikipedia.org/wiki/Optimal_Asymmetric_Encryption_Padding OAES}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |
| `$l` | **string** |  |





***

### _rsaes_oaep_decrypt

RSAES-OAEP-DECRYPT

```php
public _rsaes_oaep_decrypt(string $c, string $l = &#039;&#039;): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-7.1.2}.  The fact that the error
messages aren't distinguishable from one another hinders debugging, but, to quote from RFC3447#section-7.1.2:

   Note.  Care must be taken to ensure that an opponent cannot
   distinguish the different error conditions in Step 3.g, whether by
   error message or timing, or, more generally, learn partial
   information about the encoded message EM.  Otherwise an opponent may
   be able to obtain useful information about the decryption of the
   ciphertext C, leading to a chosen-ciphertext attack such as the one
   observed by Manger [36].

As for $l...  to quote from {@link http://tools.ietf.org/html/rfc3447#page-17}:

   Both the encryption and the decryption operations of RSAES-OAEP take
   the value of a label L as input.  In this version of PKCS #1, L is
   the empty string; other uses of the label are outside the scope of
   this document.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$c` | **string** |  |
| `$l` | **string** |  |





***

### _raw_encrypt

Raw Encryption / Decryption

```php
public _raw_encrypt(string $m): string
```

Doesn't use padding and is not recommended.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _rsaes_pkcs1_v1_5_encrypt

RSAES-PKCS1-V1_5-ENCRYPT

```php
public _rsaes_pkcs1_v1_5_encrypt(string $m): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-7.2.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _rsaes_pkcs1_v1_5_decrypt

RSAES-PKCS1-V1_5-DECRYPT

```php
public _rsaes_pkcs1_v1_5_decrypt(string $c): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-7.2.2}.

For compatibility purposes, this function departs slightly from the description given in RFC3447.
The reason being that RFC2313#section-8.1 (PKCS#1 v1.5) states that ciphertext's encrypted by the
private key should have the second byte set to either 0 or 1 and that ciphertext's encrypted by the
public key should have the second byte set to 2.  In RFC3447 (PKCS#1 v2.1), the second byte is supposed
to be 2 regardless of which key is used.  For compatibility purposes, we'll just check to make sure the
second byte is 2 or less.  If it is, we'll accept the decrypted string as valid.

As a consequence of this, a private key encrypted ciphertext produced with \phpseclib\Crypt\RSA may not decrypt
with a strictly PKCS#1 v1.5 compliant RSA implementation.  Public key encrypted ciphertext's should but
not private key encrypted ciphertext's.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$c` | **string** |  |





***

### _emsa_pss_encode

EMSA-PSS-ENCODE

```php
public _emsa_pss_encode(string $m, int $emBits): mixed
```

See {@link http://tools.ietf.org/html/rfc3447#section-9.1.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |
| `$emBits` | **int** |  |





***

### _emsa_pss_verify

EMSA-PSS-VERIFY

```php
public _emsa_pss_verify(string $m, string $em, int $emBits): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-9.1.2}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |
| `$em` | **string** |  |
| `$emBits` | **int** |  |





***

### _rsassa_pss_sign

RSASSA-PSS-SIGN

```php
public _rsassa_pss_sign(string $m): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-8.1.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _rsassa_pss_verify

RSASSA-PSS-VERIFY

```php
public _rsassa_pss_verify(string $m, string $s): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-8.1.2}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |
| `$s` | **string** |  |





***

### _emsa_pkcs1_v1_5_encode

EMSA-PKCS1-V1_5-ENCODE

```php
public _emsa_pkcs1_v1_5_encode(string $m, int $emLen): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-9.2}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |
| `$emLen` | **int** |  |





***

### _emsa_pkcs1_v1_5_encode_without_null

EMSA-PKCS1-V1_5-ENCODE (without NULL)

```php
public _emsa_pkcs1_v1_5_encode_without_null(string $m, int $emLen): string
```

Quoting https://tools.ietf.org/html/rfc8017#page-65,

"The parameters field associated with id-sha1, id-sha224, id-sha256,
 id-sha384, id-sha512, id-sha512/224, and id-sha512/256 should
 generally be omitted, but if present, it shall have a value of type
 NULL"






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |
| `$emLen` | **int** |  |





***

### _rsassa_pkcs1_v1_5_sign

RSASSA-PKCS1-V1_5-SIGN

```php
public _rsassa_pkcs1_v1_5_sign(string $m): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-8.2.1}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |





***

### _rsassa_pkcs1_v1_5_verify

RSASSA-PKCS1-V1_5-VERIFY

```php
public _rsassa_pkcs1_v1_5_verify(string $m, string $s): string
```

See {@link http://tools.ietf.org/html/rfc3447#section-8.2.2}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** |  |
| `$s` | **string** |  |





***

### setEncryptionMode

Set Encryption Mode

```php
public setEncryptionMode(int $mode): mixed
```

Valid values include self::ENCRYPTION_OAEP and self::ENCRYPTION_PKCS1.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** |  |





***

### setSignatureMode

Set Signature Mode

```php
public setSignatureMode(int $mode): mixed
```

Valid values include self::SIGNATURE_PSS and self::SIGNATURE_PKCS1






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** |  |





***

### setComment

Set public key comment.

```php
public setComment(string $comment): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$comment` | **string** |  |





***

### getComment

Get public key comment.

```php
public getComment(): string
```












***

### encrypt

Encryption

```php
public encrypt(string $plaintext): string
```

Both self::ENCRYPTION_OAEP and self::ENCRYPTION_PKCS1 both place limits on how long $plaintext can be.
If $plaintext exceeds those limits it will be broken up so that it does and the resultant ciphertext's will
be concatenated together.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plaintext` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::decrypt() - 

***

### decrypt

Decryption

```php
public decrypt(string $ciphertext): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ciphertext` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::encrypt() - 

***

### sign

Create a signature

```php
public sign(string $message): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::verify() - 

***

### verify

Verifies a signature

```php
public verify(string $message, string $signature): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |
| `$signature` | **string** |  |





**See Also:**

* \phpseclib\Crypt\self::sign() - 

***

### _extractBER

Extract raw BER from Base64 encoding

```php
public _extractBER(string $str): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***


***
> Automatically generated on 2025-03-15
