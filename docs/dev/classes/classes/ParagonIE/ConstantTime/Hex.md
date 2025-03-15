
# Hex

Class Hex



* Full name: `\ParagonIE\ConstantTime\Hex`
* This class implements:
[`\ParagonIE\ConstantTime\EncoderInterface`](./EncoderInterface.md)
* This class is an **Abstract class**




## Methods


### encode

Convert a binary string into a hexadecimal string without cache-timing
leaks

```php
public static encode(string $binString): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$binString` | **string** | (raw binary) |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### encodeUpper

Convert a binary string into a hexadecimal string without cache-timing
leaks, returning uppercase letters (as per RFC 4648)

```php
public static encodeUpper(string $binString): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$binString` | **string** | (raw binary) |




**Throws:**

- [`TypeError`](../../TypeError.md)



***

### decode

Convert a hexadecimal string into a binary string without cache-timing
leaks

```php
public static decode(string $encodedString, bool $strictPadding = false): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedString` | **string** |  |
| `$strictPadding` | **bool** |  |


**Return Value:**

(raw binary)



**Throws:**

- [`RangeException`](../../RangeException.md)



***


***
> Automatically generated on 2025-03-15
