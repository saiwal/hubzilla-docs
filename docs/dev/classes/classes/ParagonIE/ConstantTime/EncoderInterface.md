
# EncoderInterface

Interface EncoderInterface



* Full name: `\ParagonIE\ConstantTime\EncoderInterface`



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





***

### decode

Convert a binary string into a hexadecimal string without cache-timing
leaks

```php
public static decode(string $encodedString, bool $strictPadding = false): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedString` | **string** |  |
| `$strictPadding` | **bool** | Error on invalid padding |


**Return Value:**

(raw binary)




***


***
> Automatically generated on 2025-03-15
