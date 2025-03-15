***

# TimestampLastCombCodec

TimestampLastCombCodec encodes and decodes COMBs, with the timestamp as the
last 48 bits

The CombGenerator when used with the StringCodec (and, by proxy, the
TimestampLastCombCodec) adds the timestamp to the last 48 bits of the COMB.
The TimestampLastCombCodec is provided for the sake of consistency. In
practice, it is identical to the standard StringCodec but, it may be used
with the CombGenerator for additional context when reading code.

Consider the following code. By default, the codec used by UuidFactory is the
StringCodec, but here, we explicitly set the TimestampLastCombCodec. It is
redundant, but it is clear that we intend this COMB to be generated with the
timestamp appearing at the end.

``` php
$factory = new UuidFactory();

$factory->setCodec(new TimestampLastCombCodec($factory->getUuidBuilder()));

$factory->setRandomGenerator(new CombGenerator(
    $factory->getRandomGenerator(),
    $factory->getNumberConverter()
));

$timestampLastComb = $factory->uuid4();
```

* Full name: `\Ramsey\Uuid\Codec\TimestampLastCombCodec`
* Parent class: [`\Ramsey\Uuid\Codec\StringCodec`](./StringCodec.md)

**See Also:**

* https://www.informit.com/articles/printerfriendly/25862 - The Cost of GUIDs as Primary Keys






## Inherited methods


### __construct

Constructs a StringCodec

```php
public __construct(\Ramsey\Uuid\Builder\UuidBuilderInterface $builder): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$builder` | **\Ramsey\Uuid\Builder\UuidBuilderInterface** | The builder to use when encoding UUIDs |





***

### encode

Returns a hexadecimal string representation of a UuidInterface

```php
public encode(\Ramsey\Uuid\UuidInterface $uuid): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **\Ramsey\Uuid\UuidInterface** | The UUID for which to create a hexadecimal<br />string representation |


**Return Value:**

Hexadecimal string representation of a UUID




***

### encodeBinary

Returns a binary string representation of a UuidInterface

```php
public encodeBinary(\Ramsey\Uuid\UuidInterface $uuid): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **\Ramsey\Uuid\UuidInterface** | The UUID for which to create a binary string<br />representation |


**Return Value:**

Binary string representation of a UUID




***

### decode

Returns a UuidInterface derived from a hexadecimal string representation

```php
public decode(string $encodedUuid): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedUuid` | **string** | The hexadecimal string representation to<br />convert into a UuidInterface instance |


**Return Value:**

An instance of a UUID decoded from a hexadecimal
string representation



**Throws:**

- [`InvalidUuidStringException`](../Exception/InvalidUuidStringException.md)



***

### decodeBytes

Returns a UuidInterface derived from a binary string representation

```php
public decodeBytes(string $bytes): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | The binary string representation to convert into a<br />UuidInterface instance |


**Return Value:**

An instance of a UUID decoded from a binary string
representation




***

### getBuilder

Returns the UUID builder

```php
protected getBuilder(): \Ramsey\Uuid\Builder\UuidBuilderInterface
```












***

### getBytes

Returns a byte string of the UUID

```php
protected getBytes(string $encodedUuid): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encodedUuid` | **string** |  |





***


***
> Automatically generated on 2025-03-15
