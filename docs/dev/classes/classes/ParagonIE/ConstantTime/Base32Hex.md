
# Base32Hex

Class Base32Hex
[0-9][A-V]



* Full name: `\ParagonIE\ConstantTime\Base32Hex`
* Parent class: [`\ParagonIE\ConstantTime\Base32`](./Base32.md)
* This class is an **Abstract class**




## Methods


### decode5Bits

Uses bitwise operators instead of table-lookups to turn 5-bit integers
into 8-bit integers.

```php
protected static decode5Bits(int $src): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### decode5BitsUpper

Uses bitwise operators instead of table-lookups to turn 5-bit integers
into 8-bit integers.

```php
protected static decode5BitsUpper(int $src): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### encode5Bits

Uses bitwise operators instead of table-lookups to turn 8-bit integers
into 5-bit integers.

```php
protected static encode5Bits(int $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### encode5BitsUpper

Uses bitwise operators instead of table-lookups to turn 8-bit integers
into 5-bit integers.

```php
protected static encode5BitsUpper(int $src): string
```

Uppercase variant.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***


## Inherited methods


### decode

Decode a Base32-encoded string into raw binary

```php
public static decode(string $encodedString, bool $strictPadding = false): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedString` | **string** |  |
| `$strictPadding` | **bool** |  |





***

### decodeUpper

Decode an uppercase Base32-encoded string into raw binary

```php
public static decodeUpper(string $src, bool $strictPadding = false): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |
| `$strictPadding` | **bool** |  |





***

### encode

Encode into Base32 (RFC 4648)

```php
public static encode(string $binString): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$binString` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### encodeUnpadded

Encode into Base32 (RFC 4648)

```php
public static encodeUnpadded(string $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### encodeUpper

Encode into uppercase Base32 (RFC 4648)

```php
public static encodeUpper(string $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### encodeUpperUnpadded

Encode into uppercase Base32 (RFC 4648)

```php
public static encodeUpperUnpadded(string $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### decode5Bits

Uses bitwise operators instead of table-lookups to turn 5-bit integers
into 8-bit integers.

```php
protected static decode5Bits(int $src): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### decode5BitsUpper

Uses bitwise operators instead of table-lookups to turn 5-bit integers
into 8-bit integers.

```php
protected static decode5BitsUpper(int $src): int
```

Uppercase variant.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### encode5Bits

Uses bitwise operators instead of table-lookups to turn 8-bit integers
into 5-bit integers.

```php
protected static encode5Bits(int $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### encode5BitsUpper

Uses bitwise operators instead of table-lookups to turn 8-bit integers
into 5-bit integers.

```php
protected static encode5BitsUpper(int $src): string
```

Uppercase variant.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### decodeNoPadding



```php
public static decodeNoPadding(string $encodedString, bool $upper = false): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedString` | **string** |  |
| `$upper` | **bool** |  |





***

### doDecode

Base32 decoding

```php
protected static doDecode(string $src, bool $upper = false, bool $strictPadding = false): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |
| `$upper` | **bool** |  |
| `$strictPadding` | **bool** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### doEncode

Base32 Encoding

```php
protected static doEncode(string $src, bool $upper = false, bool $pad = true): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |
| `$upper` | **bool** |  |
| `$pad` | **bool** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***


***
> Automatically generated on 2025-03-15
