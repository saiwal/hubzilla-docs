***

# DegradedUuidBuilder





* Full name: `\Ramsey\Uuid\Builder\DegradedUuidBuilder`
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.
* This class implements:
[`\Ramsey\Uuid\Builder\UuidBuilderInterface`](./UuidBuilderInterface.md)



## Properties


### timeConverter



```php
private \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter
```






***

### numberConverter



```php
private \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter, \Ramsey\Uuid\Converter\TimeConverterInterface|null $timeConverter = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** | The number converter to<br />use when constructing the DegradedUuid |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface&#124;null** | The time converter to use<br />for converting timestamps extracted from a UUID to Unix timestamps |





***

### build

Builds and returns a DegradedUuid

```php
public build(\Ramsey\Uuid\Codec\CodecInterface $codec, string $bytes): \Ramsey\Uuid\DegradedUuid
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use for building this DegradedUuid instance |
| `$bytes` | **string** | The byte string from which to construct a UUID |


**Return Value:**

The DegradedUuidBuild returns an instance of Ramsey\Uuid\DegradedUuid




***


***
> Automatically generated on 2025-03-15
