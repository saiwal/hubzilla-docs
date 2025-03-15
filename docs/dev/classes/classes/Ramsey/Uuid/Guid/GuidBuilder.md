***

# GuidBuilder

GuidBuilder builds instances of Guid



* Full name: `\Ramsey\Uuid\Guid\GuidBuilder`
* This class implements:
[`\Ramsey\Uuid\Builder\UuidBuilderInterface`](../Builder/UuidBuilderInterface.md)

**See Also:**

* \Ramsey\Uuid\Guid\Guid - 



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
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** | The number converter to<br />use when constructing the Guid |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface** | The time converter to use<br />for converting timestamps extracted from a UUID to Unix timestamps |





***

### build

Builds and returns a Guid

```php
public build(\Ramsey\Uuid\Codec\CodecInterface $codec, string $bytes): \Ramsey\Uuid\Guid\Guid
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use for building this Guid instance |
| `$bytes` | **string** | The byte string from which to construct a UUID |


**Return Value:**

The GuidBuilder returns an instance of Ramsey\Uuid\Guid\Guid




***

### buildFields

Proxy method to allow injecting a mock, for testing

```php
protected buildFields(string $bytes): \Ramsey\Uuid\Guid\Fields
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** |  |





***


***
> Automatically generated on 2025-03-15
