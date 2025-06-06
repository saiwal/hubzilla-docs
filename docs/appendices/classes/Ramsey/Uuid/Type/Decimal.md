
# Decimal

A value object representing a decimal

This class exists for type-safety purposes, to ensure that decimals
returned from ramsey/uuid methods as strings are truly decimals and not some
other kind of string.

To support values as true decimals and not as floats or doubles, we store the
decimals as strings.

* Full name: `\Ramsey\Uuid\Type\Decimal`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\Ramsey\Uuid\Type\NumberInterface`](./NumberInterface.md)
* This class is a **Final class**



## Properties


### value



```php
private string $value
```






***

### isNegative



```php
private bool $isNegative
```






***

## Methods


### __construct



```php
public __construct(float|int|string|self $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **float&#124;int&#124;string&#124;self** |  |





***

### isNegative

Returns true if this number is less than zero

```php
public isNegative(): bool
```












***

### toString



```php
public toString(): string
```












***

### __toString



```php
public __toString(): string
```












***

### jsonSerialize



```php
public jsonSerialize(): string
```












***

### serialize



```php
public serialize(): string
```












***

### __serialize



```php
public __serialize(): array{string: string}
```












***

### unserialize

Constructs the object from a serialized string representation

```php
public unserialize(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | The serialized string representation of the object |





***

### __unserialize



```php
public __unserialize(array{string?: string} $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array{string?: string}** |  |





***


***
> Automatically generated on 2025-03-18
