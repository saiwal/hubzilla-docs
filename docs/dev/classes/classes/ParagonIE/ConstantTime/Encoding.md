
# Encoding

Class Encoding



* Full name: `\ParagonIE\ConstantTime\Encoding`
* This class is an **Abstract class**




## Methods


### base32Encode

RFC 4648 Base32 encoding

```php
public static base32Encode(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base32EncodeUpper

RFC 4648 Base32 encoding

```php
public static base32EncodeUpper(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base32Decode

RFC 4648 Base32 decoding

```php
public static base32Decode(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base32DecodeUpper

RFC 4648 Base32 decoding

```php
public static base32DecodeUpper(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base32HexEncode

RFC 4648 Base32 encoding

```php
public static base32HexEncode(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base32HexEncodeUpper

RFC 4648 Base32Hex encoding

```php
public static base32HexEncodeUpper(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base32HexDecode

RFC 4648 Base32Hex decoding

```php
public static base32HexDecode(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base32HexDecodeUpper

RFC 4648 Base32Hex decoding

```php
public static base32HexDecodeUpper(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base64Encode

RFC 4648 Base64 encoding

```php
public static base64Encode(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base64Decode

RFC 4648 Base64 decoding

```php
public static base64Decode(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base64EncodeDotSlash

Encode into Base64

```php
public static base64EncodeDotSlash(string $str): string
```

Base64 character set "./[A-Z][a-z][0-9]"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base64DecodeDotSlash

Decode from base64 to raw binary

```php
public static base64DecodeDotSlash(string $str): string
```

Base64 character set "./[A-Z][a-z][0-9]"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`RangeException`](../../RangeException.md)

- [`TypeError`](../../TypeError.md)



***

### base64EncodeDotSlashOrdered

Encode into Base64

```php
public static base64EncodeDotSlashOrdered(string $str): string
```

Base64 character set "[.-9][A-Z][a-z]" or "./[0-9][A-Z][a-z]"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### base64DecodeDotSlashOrdered

Decode from base64 to raw binary

```php
public static base64DecodeDotSlashOrdered(string $str): string
```

Base64 character set "[.-9][A-Z][a-z]" or "./[0-9][A-Z][a-z]"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`RangeException`](../../RangeException.md)

- [`TypeError`](../../TypeError.md)



***

### hexEncode

Convert a binary string into a hexadecimal string without cache-timing
leaks

```php
public static hexEncode(string $bin_string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bin_string` | **string** | (raw binary) |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### hexDecode

Convert a hexadecimal string into a binary string without cache-timing
leaks

```php
public static hexDecode(string $hex_string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hex_string` | **string** |  |


**Return Value:**

(raw binary)



**Throws:**

- [`RangeException`](../../RangeException.md)



***

### hexEncodeUpper

Convert a binary string into a hexadecimal string without cache-timing
leaks

```php
public static hexEncodeUpper(string $bin_string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bin_string` | **string** | (raw binary) |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### hexDecodeUpper

Convert a binary string into a hexadecimal string without cache-timing
leaks

```php
public static hexDecodeUpper(string $bin_string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bin_string` | **string** | (raw binary) |





***


***
> Automatically generated on 2025-03-15
