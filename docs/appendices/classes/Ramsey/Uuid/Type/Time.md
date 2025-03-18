
# Time

A value object representing a timestamp

This class exists for type-safety purposes, to ensure that timestamps used
by ramsey/uuid are truly timestamp integers and not some other kind of string
or integer.

* Full name: `\Ramsey\Uuid\Type\Time`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\Ramsey\Uuid\Type\TypeInterface`](./TypeInterface.md)
* This class is a **Final class**



## Properties


### seconds



```php
private \Ramsey\Uuid\Type\Integer $seconds
```






***

### microseconds



```php
private \Ramsey\Uuid\Type\Integer $microseconds
```






***

## Methods


### __construct



```php
public __construct(float|int|string|\Ramsey\Uuid\Type\Integer $seconds, float|int|string|\Ramsey\Uuid\Type\Integer $microseconds): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$seconds` | **float&#124;int&#124;string&#124;\Ramsey\Uuid\Type\Integer** |  |
| `$microseconds` | **float&#124;int&#124;string&#124;\Ramsey\Uuid\Type\Integer** |  |





***

### getSeconds



```php
public getSeconds(): \Ramsey\Uuid\Type\Integer
```












***

### getMicroseconds



```php
public getMicroseconds(): \Ramsey\Uuid\Type\Integer
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
public jsonSerialize(): string[]
```












***

### serialize



```php
public serialize(): string
```












***

### __serialize



```php
public __serialize(): array{seconds: string, microseconds: string}
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
public __unserialize(array{seconds?: string, microseconds?: string} $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array{seconds?: string, microseconds?: string}** |  |





***


***
> Automatically generated on 2025-03-18
