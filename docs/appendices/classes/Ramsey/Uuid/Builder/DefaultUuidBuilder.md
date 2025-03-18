
# DefaultUuidBuilder

UuidBuilder builds instances of RFC 4122 UUIDs



* Full name: `\Ramsey\Uuid\Builder\DefaultUuidBuilder`
* Parent class: [`\Ramsey\Uuid\Rfc4122\UuidBuilder`](../Rfc4122/UuidBuilder.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct

Constructs the DefaultUuidBuilder

```php
public __construct(\Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter, \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter, \Ramsey\Uuid\Converter\TimeConverterInterface|null $unixTimeConverter = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** | The number converter to<br />use when constructing the Uuid |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface** | The time converter to use<br />for converting Gregorian time extracted from version 1, 2, and 6<br />UUIDs to Unix timestamps |
| `$unixTimeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface&#124;null** | The time converter<br />to use for converter Unix Epoch time extracted from version 7 UUIDs<br />to Unix timestamps |





***

### build

Builds and returns a Uuid

```php
public build(\Ramsey\Uuid\Codec\CodecInterface $codec, string $bytes): \Ramsey\Uuid\Rfc4122\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use for building this Uuid instance |
| `$bytes` | **string** | The byte string from which to construct a UUID |


**Return Value:**

UuidBuilder returns instances of Rfc4122UuidInterface




***

### buildFields

Proxy method to allow injecting a mock, for testing

```php
protected buildFields(string $bytes): \Ramsey\Uuid\Rfc4122\FieldsInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** |  |





***


***
> Automatically generated on 2025-03-18
