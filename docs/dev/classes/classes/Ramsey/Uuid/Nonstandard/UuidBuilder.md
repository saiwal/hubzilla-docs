
# UuidBuilder

Nonstandard\UuidBuilder builds instances of Nonstandard\Uuid



* Full name: `\Ramsey\Uuid\Nonstandard\UuidBuilder`
* This class implements:
[`\Ramsey\Uuid\Builder\UuidBuilderInterface`](../Builder/UuidBuilderInterface.md)



## Properties


### numberConverter



```php
private \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter
```






***

### timeConverter



```php
private \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter, \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** | The number converter to<br />use when constructing the Nonstandard\Uuid |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface** | The time converter to use<br />for converting timestamps extracted from a UUID to Unix timestamps |





***

### build

Builds and returns a Nonstandard\Uuid

```php
public build(\Ramsey\Uuid\Codec\CodecInterface $codec, string $bytes): \Ramsey\Uuid\Nonstandard\Uuid
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use for building this instance |
| `$bytes` | **string** | The byte string from which to construct a UUID |


**Return Value:**

The Nonstandard\UuidBuilder returns an instance of
Nonstandard\Uuid




***

### buildFields

Proxy method to allow injecting a mock, for testing

```php
protected buildFields(string $bytes): \Ramsey\Uuid\Nonstandard\Fields
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** |  |





***


***
> Automatically generated on 2025-03-15
