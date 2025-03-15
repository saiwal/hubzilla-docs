
# Hexadecimal

A value object representing a hexadecimal number

This class exists for type-safety purposes, to ensure that hexadecimal numbers
returned from ramsey/uuid methods as strings are truly hexadecimal and not some
other kind of string.

* Full name: `\Ramsey\Uuid\Type\Hexadecimal`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\Ramsey\Uuid\Type\TypeInterface`](./TypeInterface.md)
* This class is a **Final class**



## Properties


### value



```php
private string $value
```






***

## Methods


### __construct



```php
public __construct(self|string $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **self&#124;string** | The hexadecimal value to store |





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

### prepareValue



```php
private prepareValue(string $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





***


***
> Automatically generated on 2025-03-15
