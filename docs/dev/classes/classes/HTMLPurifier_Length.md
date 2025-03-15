
# HTMLPurifier_Length

Represents a measurable length, with a string numeric magnitude
and a unit. This object is immutable.



* Full name: `\HTMLPurifier_Length`



## Properties


### n

String numeric magnitude.

```php
protected $n
```






***

### unit

String unit. False is permitted if $n = 0.

```php
protected $unit
```






***

### isValid

Whether or not this length is valid. Null if not calculated yet.

```php
protected $isValid
```






***

### allowedUnits

Array Lookup array of units recognized by CSS 3

```php
protected static $allowedUnits
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(string $n = &#039;0&#039;, bool|string $u = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **string** | Magnitude |
| `$u` | **bool&#124;string** | Unit |





***

### make



```php
public static make(string $s): \HTMLPurifier_Length
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **string** | Unit string, like &#039;2em&#039; or &#039;3.4in&#039; |





***

### validate

Validates the number and unit.

```php
protected validate(): bool
```












***

### toString

Returns string representation of number.

```php
public toString(): string
```












***

### getN

Retrieves string numeric magnitude.

```php
public getN(): string
```












***

### getUnit

Retrieves string unit.

```php
public getUnit(): string
```












***

### isValid

Returns true if this length unit is valid.

```php
public isValid(): bool
```












***

### compareTo

Compares two lengths, and returns 1 if greater, -1 if less and 0 if equal.

```php
public compareTo(\HTMLPurifier_Length $l): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$l` | **\HTMLPurifier_Length** |  |





***


***
> Automatically generated on 2025-03-15
