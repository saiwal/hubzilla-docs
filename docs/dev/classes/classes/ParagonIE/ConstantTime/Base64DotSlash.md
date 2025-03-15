
# Base64DotSlash

Class Base64DotSlash
./[A-Z][a-z][0-9]



* Full name: `\ParagonIE\ConstantTime\Base64DotSlash`
* Parent class: [`\ParagonIE\ConstantTime\Base64`](./Base64.md)
* This class is an **Abstract class**




## Methods


### decode6Bits

Uses bitwise operators instead of table-lookups to turn 6-bit integers
into 8-bit integers.

```php
protected static decode6Bits(int $src): int
```

Base64 character set:
./         [A-Z]      [a-z]     [0-9]
0x2e-0x2f, 0x41-0x5a, 0x61-0x7a, 0x30-0x39

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### encode6Bits

Uses bitwise operators instead of table-lookups to turn 8-bit integers
into 6-bit integers.

```php
protected static encode6Bits(int $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***


## Inherited methods


### encode

Encode into Base64

```php
public static encode(string $binString): string
```

Base64 character set "[A-Z][a-z][0-9]+/"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$binString` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### encodeUnpadded

Encode into Base64, no = padding

```php
public static encodeUnpadded(string $src): string
```

Base64 character set "[A-Z][a-z][0-9]+/"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### doEncode



```php
protected static doEncode(string $src, bool $pad = true): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **string** |  |
| `$pad` | **bool** | Include = padding? |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### decode

decode from base64 into binary

```php
public static decode(string $encodedString, bool $strictPadding = false): string
```

Base64 character set "./[A-Z][a-z][0-9]"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedString` | **string** |  |
| `$strictPadding` | **bool** |  |




**Throws:**

- [`RangeException`](../../RangeException.md)

- [`TypeError`](../../TypeError.md)



***

### decodeNoPadding



```php
public static decodeNoPadding(string $encodedString): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedString` | **string** |  |





***

### decode6Bits

Uses bitwise operators instead of table-lookups to turn 6-bit integers
into 8-bit integers.

```php
protected static decode6Bits(int $src): int
```

Base64 character set:
[A-Z]      [a-z]      [0-9]      +     /
0x41-0x5a, 0x61-0x7a, 0x30-0x39, 0x2b, 0x2f

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***

### encode6Bits

Uses bitwise operators instead of table-lookups to turn 8-bit integers
into 6-bit integers.

```php
protected static encode6Bits(int $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **int** |  |





***


***
> Automatically generated on 2025-03-15
