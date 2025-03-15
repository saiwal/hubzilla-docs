
# Calculator

Provides helpers for bcmath-based arithmetic.

The bcmath extension provides support for arbitrary precision arithmetic,
which does not suffer from the precision loses that make floating point
arithmetic unsafe for eCommerce.

Important: All numbers must be passed as strings.

* Full name: `\CommerceGuys\Intl\Calculator`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**




## Methods


### add

Adds the second number to the first number.

```php
public static add(string $first_number, string $second_number, int $scale = 6): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$first_number` | **string** | The first number. |
| `$second_number` | **string** | The second number. |
| `$scale` | **int** | The maximum number of digits after the<br />decimal place. Any digit after $scale will<br />be truncated. |


**Return Value:**

The result.




***

### subtract

Subtracts the second number from the first number.

```php
public static subtract(string $first_number, string $second_number, int $scale = 6): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$first_number` | **string** | The first number. |
| `$second_number` | **string** | The second number. |
| `$scale` | **int** | The maximum number of digits after the<br />decimal place. Any digit after $scale will<br />be truncated. |


**Return Value:**

The result.




***

### multiply

Multiplies the first number by the second number.

```php
public static multiply(string $first_number, string $second_number, int $scale = 6): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$first_number` | **string** | The first number. |
| `$second_number` | **string** | The second number. |
| `$scale` | **int** | The maximum number of digits after the<br />decimal place. Any digit after $scale will<br />be truncated. |


**Return Value:**

The result.




***

### divide

Divides the first number by the second number.

```php
public static divide(string $first_number, string $second_number, int $scale = 6): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$first_number` | **string** | The first number. |
| `$second_number` | **string** | The second number. |
| `$scale` | **int** | The maximum number of digits after the<br />decimal place. Any digit after $scale will<br />be truncated. |


**Return Value:**

The result.




***

### ceil

Calculates the next highest whole value of a number.

```php
public static ceil(string $number): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |


**Return Value:**

The result.




***

### floor

Calculates the next lowest whole value of a number.

```php
public static floor(string $number): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |


**Return Value:**

The result.




***

### round

Rounds the given number.

```php
public static round(string $number, int $precision, int $mode = PHP_ROUND_HALF_UP): string
```

Replicates PHP's support for rounding to the nearest even/odd number
even if that number is decimal ($precision > 0).

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |
| `$precision` | **int** | The number of decimals to round to. |
| `$mode` | **int** | The rounding mode. One of the following constants:<br />PHP_ROUND_HALF_UP, PHP_ROUND_HALF_DOWN,<br />PHP_ROUND_HALF_EVEN, PHP_ROUND_HALF_ODD. |


**Return Value:**

The rounded number.



**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### compare

Compares the first number to the second number.

```php
public static compare(string $first_number, string $second_number, int $scale = 6): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$first_number` | **string** | The first number. |
| `$second_number` | **string** | The second number. |
| `$scale` | **int** | The maximum number of digits after the<br />decimal place. Any digit after $scale will<br />be truncated. |


**Return Value:**

0 if both numbers are equal, 1 if the first one is greater,
-1 otherwise.




***

### trim

Trims the given number.

```php
public static trim(string $number): string
```

By default bcmath returns numbers with the number of digits according
to $scale. This means that bcadd('2', '2', 6) will return '4.00000'.
Trimming the number removes the excess zeroes.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number to trim. |


**Return Value:**

The trimmed number.




***

### assertNumberFormat

Assert that the given number is a numeric string value.

```php
public static assertNumberFormat(string $number): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number to check. |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***


***
> Automatically generated on 2025-03-15
