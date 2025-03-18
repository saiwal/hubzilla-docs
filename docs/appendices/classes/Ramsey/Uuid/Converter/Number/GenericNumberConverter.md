
# GenericNumberConverter

GenericNumberConverter uses the provided calculator to convert decimal
numbers to and from hexadecimal values



* Full name: `\Ramsey\Uuid\Converter\Number\GenericNumberConverter`
* This class implements:
[`\Ramsey\Uuid\Converter\NumberConverterInterface`](../NumberConverterInterface.md)



## Properties


### calculator



```php
private \Ramsey\Uuid\Math\CalculatorInterface $calculator
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Math\CalculatorInterface $calculator): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calculator` | **\Ramsey\Uuid\Math\CalculatorInterface** |  |





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
