
# DegradedNumberConverter

Previously used to integrate moontoast/math as a bignum arithmetic library,
BigNumberConverter is deprecated in favor of GenericNumberConverter



* Full name: `\Ramsey\Uuid\Converter\Number\DegradedNumberConverter`
* Parent class: [`\Ramsey\Uuid\Converter\Number\BigNumberConverter`](./BigNumberConverter.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct



```php
public __construct(): mixed
```












***

### fromHex

Converts a hexadecimal number into an string integer representation of
the number

```php
public fromHex(string $hex): string
```








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
> Automatically generated on 2025-03-18
