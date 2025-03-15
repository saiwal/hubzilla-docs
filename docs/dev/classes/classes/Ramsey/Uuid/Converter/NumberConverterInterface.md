***

# NumberConverterInterface

A number converter converts UUIDs from hexadecimal characters into
representations of integers and vice versa



* Full name: `\Ramsey\Uuid\Converter\NumberConverterInterface`



## Methods


### fromHex

Converts a hexadecimal number into an string integer representation of
the number

```php
public fromHex(string $hex): string
```

The integer representation returned is a string representation of the
integer, to accommodate unsigned integers greater than PHP_INT_MAX.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hex` | **string** | The hexadecimal string representation to convert |


**Return Value:**

String representation of an integer




***

### toHex

Converts a string integer representation into a hexadecimal string
representation of the number

```php
public toHex(string $number): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | A string integer representation to convert; this<br />must be a numeric string to accommodate unsigned integers greater<br />than PHP_INT_MAX. |


**Return Value:**

Hexadecimal string




***


***
> Automatically generated on 2025-03-15
