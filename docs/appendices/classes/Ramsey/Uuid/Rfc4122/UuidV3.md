
# UuidV3

Version 3 UUIDs are named-based, using combination of a namespace and name
that are hashed into a 128-bit unsigned integer using MD5



* Full name: `\Ramsey\Uuid\Rfc4122\UuidV3`
* Parent class: [`\Ramsey\Uuid\Uuid`](../Uuid.md)
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\Ramsey\Uuid\Rfc4122\UuidInterface`](./UuidInterface.md)
* This class is a **Final class**




## Methods


### __construct

Creates a version 3 (name-based, MD5-hashed) UUID

```php
public __construct(\Ramsey\Uuid\Rfc4122\FieldsInterface $fields, \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter, \Ramsey\Uuid\Codec\CodecInterface $codec, \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fields` | **\Ramsey\Uuid\Rfc4122\FieldsInterface** | The fields from which to construct a UUID |
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** | The number converter to use<br />for converting hex values to/from integers |
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use when encoding or decoding<br />UUID strings |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface** | The time converter to use<br />for converting timestamps extracted from a UUID to unix timestamps |





***


## Inherited methods


### getClockSeqHiAndReserved



```php
public getClockSeqHiAndReserved(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSeqHiAndReservedHex



```php
public getClockSeqHiAndReservedHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSeqLow



```php
public getClockSeqLow(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSeqLowHex



```php
public getClockSeqLowHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSequence



```php
public getClockSequence(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSequenceHex



```php
public getClockSequenceHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getNumberConverter



```php
public getNumberConverter(): \Ramsey\Uuid\Converter\NumberConverterInterface
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getDateTime



```php
public getDateTime(): \DateTimeImmutable
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.




**Return Value:**

An immutable instance of DateTimeInterface



**Throws:**
<p>if UUID is not time-based</p>

- [`UnsupportedOperationException`](../Exception/UnsupportedOperationException.md)
<p>if DateTime throws an exception/error</p>

- [`DateTimeException`](../Exception/DateTimeException.md)



***

### getFieldsHex



```php
public getFieldsHex(): string[]
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getLeastSignificantBits



```php
public getLeastSignificantBits(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getLeastSignificantBitsHex



```php
public getLeastSignificantBitsHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getMostSignificantBits



```php
public getMostSignificantBits(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getMostSignificantBitsHex



```php
public getMostSignificantBitsHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getNode



```php
public getNode(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getNodeHex



```php
public getNodeHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeHiAndVersion



```php
public getTimeHiAndVersion(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeHiAndVersionHex



```php
public getTimeHiAndVersionHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeLow



```php
public getTimeLow(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeLowHex



```php
public getTimeLowHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeMid



```php
public getTimeMid(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeMidHex



```php
public getTimeMidHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimestamp



```php
public getTimestamp(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimestampHex



```php
public getTimestampHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getVariant



```php
public getVariant(): ?int
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getVersion



```php
public getVersion(): ?int
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### __construct

Creates a universally unique identifier (UUID) from an array of fields

```php
public __construct(\Ramsey\Uuid\Rfc4122\FieldsInterface $fields, \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter, \Ramsey\Uuid\Codec\CodecInterface $codec, \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter): mixed
```

Unless you're making advanced use of this library to generate identifiers
that deviate from RFC 4122, you probably do not want to instantiate a
UUID directly. Use the static methods, instead:

```
use Ramsey\Uuid\Uuid;

$timeBasedUuid = Uuid::uuid1();
$namespaceMd5Uuid = Uuid::uuid3(Uuid::NAMESPACE_URL, 'http://php.net/');
$randomUuid = Uuid::uuid4();
$namespaceSha1Uuid = Uuid::uuid5(Uuid::NAMESPACE_URL, 'http://php.net/');
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fields` | **\Ramsey\Uuid\Rfc4122\FieldsInterface** | The fields from which to construct a UUID |
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** | The number converter to use<br />for converting hex values to/from integers |
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use when encoding or decoding<br />UUID strings |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface** | The time converter to use<br />for converting timestamps extracted from a UUID to unix timestamps |





***

### __toString

Casts the UUID to the string standard representation

```php
public __toString(): string
```












***

### jsonSerialize

Converts the UUID to a string for JSON serialization

```php
public jsonSerialize(): string
```












***

### serialize

Converts the UUID to a string for PHP serialization

```php
public serialize(): string
```












***

### __serialize



```php
public __serialize(): array{bytes: string}
```












***

### unserialize

Re-constructs the object from its serialized form

```php
public unserialize(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | The serialized PHP string to unserialize into<br />a UuidInterface instance |





***

### __unserialize



```php
public __unserialize(array{bytes?: string} $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array{bytes?: string}** |  |





***

### compareTo

Returns -1, 0, or 1 if the UUID is less than, equal to, or greater than
the other UUID

```php
public compareTo(\Ramsey\Uuid\UuidInterface $other): int&lt;-1, 1&gt;
```

The first of two UUIDs is greater than the second if the most
significant field in which the UUIDs differ is greater for the first
UUID.

* Q. What's the value of being able to sort UUIDs?
* A. Use them as keys in a B-Tree or similar mapping.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\Ramsey\Uuid\UuidInterface** | The UUID to compare |


**Return Value:**

-1, 0, or 1 if the UUID is less than, equal to, or greater than $other




***

### equals

Returns true if the UUID is equal to the provided object

```php
public equals(?object $other): bool
```

The result is true if and only if the argument is not null, is a UUID
object, has the same variant, and contains the same value, bit for bit,
as the UUID.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **?object** | An object to test for equality with this UUID |


**Return Value:**

True if the other object is equal to this UUID




***

### getBytes

Returns the binary string representation of the UUID

```php
public getBytes(): string
```












***

### getFields

Returns the fields that comprise this UUID

```php
public getFields(): \Ramsey\Uuid\Fields\FieldsInterface
```












***

### getHex

Returns the hexadecimal representation of the UUID

```php
public getHex(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getInteger

Returns the integer representation of the UUID

```php
public getInteger(): \Ramsey\Uuid\Type\Integer
```












***

### getUrn

Returns the string standard representation of the UUID as a URN

```php
public getUrn(): string
```












***

### toString

Returns the string standard representation of the UUID

```php
public toString(): string
```












***

### getFactory

Returns the factory used to create UUIDs

```php
public static getFactory(): \Ramsey\Uuid\UuidFactoryInterface
```



* This method is **static**.








***

### setFactory

Sets the factory used to create UUIDs

```php
public static setFactory(\Ramsey\Uuid\UuidFactoryInterface $factory): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$factory` | **\Ramsey\Uuid\UuidFactoryInterface** | A factory that will be used by this<br />class to create UUIDs |





***

### fromBytes

Creates a UUID from a byte string

```php
public static fromBytes(string $bytes): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | A binary string |


**Return Value:**

A UuidInterface instance created from a binary
string representation




***

### fromString

Creates a UUID from the string standard representation

```php
public static fromString(string $uuid): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **string** | A hexadecimal string |


**Return Value:**

A UuidInterface instance created from a hexadecimal
string representation




***

### fromDateTime

Creates a UUID from a DateTimeInterface instance

```php
public static fromDateTime(\DateTimeInterface $dateTime, \Ramsey\Uuid\Type\Hexadecimal|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dateTime` | **\DateTimeInterface** | The date and time |
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;null** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 1 UUID created from a DateTimeInterface instance




***

### fromHexadecimal

Creates a UUID from the Hexadecimal object

```php
public static fromHexadecimal(\Ramsey\Uuid\Type\Hexadecimal $hex): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hex` | **\Ramsey\Uuid\Type\Hexadecimal** | Hexadecimal object representing a hexadecimal number |


**Return Value:**

A UuidInterface instance created from the Hexadecimal
object representing a hexadecimal number




***

### fromInteger

Creates a UUID from a 128-bit integer string

```php
public static fromInteger(string $integer): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$integer` | **string** | String representation of 128-bit integer |


**Return Value:**

A UuidInterface instance created from the string
representation of a 128-bit integer




***

### isValid

Returns true if the provided string is a valid UUID

```php
public static isValid(string $uuid): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **string** | A string to validate as a UUID |


**Return Value:**

True if the string is a valid UUID, false otherwise




***

### uuid1

Returns a version 1 (Gregorian time) UUID from a host ID, sequence number,
and the current time

```php
public static uuid1(\Ramsey\Uuid\Type\Hexadecimal|int|string|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;int&#124;string&#124;null** | A 48-bit number representing the<br />hardware address; this number may be represented as an integer or a<br />hexadecimal string |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates that<br />could arise when the clock is set backwards in time or if the node ID<br />changes |


**Return Value:**

A UuidInterface instance that represents a
version 1 UUID




***

### uuid2

Returns a version 2 (DCE Security) UUID from a local domain, local
identifier, host ID, clock sequence, and the current time

```php
public static uuid2(int $localDomain, \Ramsey\Uuid\Type\Integer|null $localIdentifier = null, \Ramsey\Uuid\Type\Hexadecimal|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$localDomain` | **int** | The local domain to use when generating bytes,<br />according to DCE Security |
| `$localIdentifier` | **\Ramsey\Uuid\Type\Integer&#124;null** | The local identifier for the<br />given domain; this may be a UID or GID on POSIX systems, if the local<br />domain is person or group, or it may be a site-defined identifier<br />if the local domain is org |
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;null** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes (in a version 2 UUID, the lower 8 bits of this number<br />are replaced with the domain). |


**Return Value:**

A UuidInterface instance that represents a
version 2 UUID




***

### uuid3

Returns a version 3 (name-based) UUID based on the MD5 hash of a
namespace ID and a name

```php
public static uuid3(string|\Ramsey\Uuid\UuidInterface $ns, string $name): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ns` | **string&#124;\Ramsey\Uuid\UuidInterface** | The namespace (must be a valid UUID) |
| `$name` | **string** | The name to use for creating a UUID |


**Return Value:**

A UuidInterface instance that represents a
version 3 UUID




***

### uuid4

Returns a version 4 (random) UUID

```php
public static uuid4(): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.





**Return Value:**

A UuidInterface instance that represents a
version 4 UUID




***

### uuid5

Returns a version 5 (name-based) UUID based on the SHA-1 hash of a
namespace ID and a name

```php
public static uuid5(string|\Ramsey\Uuid\UuidInterface $ns, string $name): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ns` | **string&#124;\Ramsey\Uuid\UuidInterface** | The namespace (must be a valid UUID) |
| `$name` | **string** | The name to use for creating a UUID |


**Return Value:**

A UuidInterface instance that represents a
version 5 UUID




***

### uuid6

Returns a version 6 (reordered time) UUID from a host ID, sequence number,
and the current time

```php
public static uuid6(\Ramsey\Uuid\Type\Hexadecimal|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;null** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates that<br />could arise when the clock is set backwards in time or if the node ID<br />changes |


**Return Value:**

A UuidInterface instance that represents a
version 6 UUID




***

### uuid7

Returns a version 7 (Unix Epoch time) UUID

```php
public static uuid7(\DateTimeInterface|null $dateTime = null): \Ramsey\Uuid\UuidInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dateTime` | **\DateTimeInterface&#124;null** | An optional date/time from which<br />to create the version 7 UUID. If not provided, the UUID is generated<br />using the current date/time. |


**Return Value:**

A UuidInterface instance that represents a
version 7 UUID




***

### uuid8

Returns a version 8 (custom) UUID

```php
public static uuid8(string $bytes): \Ramsey\Uuid\UuidInterface
```

The bytes provided may contain any value according to your application's
needs. Be aware, however, that other applications may not understand the
semantics of the value.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | A 16-byte octet string. This is an open blob<br />of data that you may fill with 128 bits of information. Be aware,<br />however, bits 48 through 51 will be replaced with the UUID version<br />field, and bits 64 and 65 will be replaced with the UUID variant. You<br />MUST NOT rely on these bits for your application needs. |


**Return Value:**

A UuidInterface instance that represents a
version 8 UUID




***


***
> Automatically generated on 2025-03-18
