***

# UuidFactory





* Full name: `\Ramsey\Uuid\UuidFactory`
* This class implements:
[`\Ramsey\Uuid\UuidFactoryInterface`](./UuidFactoryInterface.md)



## Properties


### codec



```php
private \Ramsey\Uuid\Codec\CodecInterface $codec
```






***

### dceSecurityGenerator



```php
private \Ramsey\Uuid\Generator\DceSecurityGeneratorInterface $dceSecurityGenerator
```






***

### nameGenerator



```php
private \Ramsey\Uuid\Generator\NameGeneratorInterface $nameGenerator
```






***

### nodeProvider



```php
private \Ramsey\Uuid\Provider\NodeProviderInterface $nodeProvider
```






***

### numberConverter



```php
private \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter
```






***

### randomGenerator



```php
private \Ramsey\Uuid\Generator\RandomGeneratorInterface $randomGenerator
```






***

### timeConverter



```php
private \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter
```






***

### timeGenerator



```php
private \Ramsey\Uuid\Generator\TimeGeneratorInterface $timeGenerator
```






***

### unixTimeGenerator



```php
private \Ramsey\Uuid\Generator\TimeGeneratorInterface $unixTimeGenerator
```






***

### uuidBuilder



```php
private \Ramsey\Uuid\Builder\UuidBuilderInterface $uuidBuilder
```






***

### validator



```php
private \Ramsey\Uuid\Validator\ValidatorInterface $validator
```






***

### isDefaultFeatureSet



```php
private bool $isDefaultFeatureSet
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\FeatureSet|null $features = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$features` | **\Ramsey\Uuid\FeatureSet&#124;null** | A set of available features in the current environment |





***

### getCodec

Returns the codec used by this factory

```php
public getCodec(): \Ramsey\Uuid\Codec\CodecInterface
```












***

### setCodec

Sets the codec to use for this factory

```php
public setCodec(\Ramsey\Uuid\Codec\CodecInterface $codec): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | A UUID encoder-decoder |





***

### getNameGenerator

Returns the name generator used by this factory

```php
public getNameGenerator(): \Ramsey\Uuid\Generator\NameGeneratorInterface
```












***

### setNameGenerator

Sets the name generator to use for this factory

```php
public setNameGenerator(\Ramsey\Uuid\Generator\NameGeneratorInterface $nameGenerator): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$nameGenerator` | **\Ramsey\Uuid\Generator\NameGeneratorInterface** | A generator to generate<br />binary data, based on a namespace and name |





***

### getNodeProvider

Returns the node provider used by this factory

```php
public getNodeProvider(): \Ramsey\Uuid\Provider\NodeProviderInterface
```












***

### getRandomGenerator

Returns the random generator used by this factory

```php
public getRandomGenerator(): \Ramsey\Uuid\Generator\RandomGeneratorInterface
```












***

### getTimeGenerator

Returns the time generator used by this factory

```php
public getTimeGenerator(): \Ramsey\Uuid\Generator\TimeGeneratorInterface
```












***

### setTimeGenerator

Sets the time generator to use for this factory

```php
public setTimeGenerator(\Ramsey\Uuid\Generator\TimeGeneratorInterface $generator): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$generator` | **\Ramsey\Uuid\Generator\TimeGeneratorInterface** | A generator to generate binary<br />data, based on the time |





***

### getDceSecurityGenerator

Returns the DCE Security generator used by this factory

```php
public getDceSecurityGenerator(): \Ramsey\Uuid\Generator\DceSecurityGeneratorInterface
```












***

### setDceSecurityGenerator

Sets the DCE Security generator to use for this factory

```php
public setDceSecurityGenerator(\Ramsey\Uuid\Generator\DceSecurityGeneratorInterface $generator): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$generator` | **\Ramsey\Uuid\Generator\DceSecurityGeneratorInterface** | A generator to generate<br />binary data, based on a local domain and local identifier |





***

### getNumberConverter

Returns the number converter used by this factory

```php
public getNumberConverter(): \Ramsey\Uuid\Converter\NumberConverterInterface
```












***

### setRandomGenerator

Sets the random generator to use for this factory

```php
public setRandomGenerator(\Ramsey\Uuid\Generator\RandomGeneratorInterface $generator): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$generator` | **\Ramsey\Uuid\Generator\RandomGeneratorInterface** | A generator to generate binary<br />data, based on some random input |





***

### setNumberConverter

Sets the number converter to use for this factory

```php
public setNumberConverter(\Ramsey\Uuid\Converter\NumberConverterInterface $converter): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$converter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** | A converter to use for working<br />with large integers (i.e. integers greater than PHP_INT_MAX) |





***

### getUuidBuilder

Returns the UUID builder used by this factory

```php
public getUuidBuilder(): \Ramsey\Uuid\Builder\UuidBuilderInterface
```












***

### setUuidBuilder

Sets the UUID builder to use for this factory

```php
public setUuidBuilder(\Ramsey\Uuid\Builder\UuidBuilderInterface $builder): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$builder` | **\Ramsey\Uuid\Builder\UuidBuilderInterface** | A builder for constructing instances<br />of UuidInterface |





***

### getValidator

Returns the validator to use for the factory

```php
public getValidator(): \Ramsey\Uuid\Validator\ValidatorInterface
```












***

### setValidator

Sets the validator to use for this factory

```php
public setValidator(\Ramsey\Uuid\Validator\ValidatorInterface $validator): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$validator` | **\Ramsey\Uuid\Validator\ValidatorInterface** | A validator to use for validating<br />whether a string is a valid UUID |





***

### fromBytes

Creates a UUID from a byte string

```php
public fromBytes(string $bytes): \Ramsey\Uuid\UuidInterface
```








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
public fromString(string $uuid): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **string** | A hexadecimal string |


**Return Value:**

A UuidInterface instance created from a hexadecimal
string representation




***

### fromInteger

Creates a UUID from a 128-bit integer string

```php
public fromInteger(string $integer): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$integer` | **string** | String representation of 128-bit integer |


**Return Value:**

A UuidInterface instance created from the string
representation of a 128-bit integer




***

### fromDateTime

Creates a UUID from a DateTimeInterface instance

```php
public fromDateTime(\DateTimeInterface $dateTime, ?\Ramsey\Uuid\Type\Hexadecimal $node = null, ?int $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dateTime` | **\DateTimeInterface** | The date and time |
| `$node` | **?\Ramsey\Uuid\Type\Hexadecimal** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **?int** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 1 UUID created from a DateTimeInterface instance




***

### fromHexadecimal



```php
public fromHexadecimal(\Ramsey\Uuid\Type\Hexadecimal $hex): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hex` | **\Ramsey\Uuid\Type\Hexadecimal** |  |





***

### uuid1

Returns a version 1 (Gregorian time) UUID from a host ID, sequence number,
and the current time

```php
public uuid1(mixed $node = null, ?int $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **mixed** | A 48-bit number representing the<br />hardware address; this number may be represented as an integer or a<br />hexadecimal string |
| `$clockSeq` | **?int** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 1 UUID




***

### uuid2

Returns a version 2 (DCE Security) UUID from a local domain, local
identifier, host ID, clock sequence, and the current time

```php
public uuid2(int $localDomain, ?\Ramsey\Uuid\Type\Integer $localIdentifier = null, ?\Ramsey\Uuid\Type\Hexadecimal $node = null, ?int $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$localDomain` | **int** | The local domain to use when generating bytes,<br />according to DCE Security |
| `$localIdentifier` | **?\Ramsey\Uuid\Type\Integer** | The local identifier for the<br />given domain; this may be a UID or GID on POSIX systems, if the local<br />domain is person or group, or it may be a site-defined identifier<br />if the local domain is org |
| `$node` | **?\Ramsey\Uuid\Type\Hexadecimal** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **?int** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 2 UUID




***

### uuid3

Returns a version 3 (name-based) UUID based on the MD5 hash of a
namespace ID and a name

```php
public uuid3(mixed $ns, string $name): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ns` | **mixed** | The namespace (must be a valid UUID) |
| `$name` | **string** | The name to use for creating a UUID |


**Return Value:**

A UuidInterface instance that represents a
version 3 UUID




***

### uuid4

Returns a version 4 (random) UUID

```php
public uuid4(): \Ramsey\Uuid\UuidInterface
```









**Return Value:**

A UuidInterface instance that represents a
version 4 UUID




***

### uuid5

Returns a version 5 (name-based) UUID based on the SHA-1 hash of a
namespace ID and a name

```php
public uuid5(mixed $ns, string $name): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ns` | **mixed** | The namespace (must be a valid UUID) |
| `$name` | **string** | The name to use for creating a UUID |


**Return Value:**

A UuidInterface instance that represents a
version 5 UUID




***

### uuid6

Returns a version 6 (reordered time) UUID from a host ID, sequence number,
and the current time

```php
public uuid6(?\Ramsey\Uuid\Type\Hexadecimal $node = null, ?int $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **?\Ramsey\Uuid\Type\Hexadecimal** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **?int** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 6 UUID




***

### uuid7

Returns a version 7 (Unix Epoch time) UUID

```php
public uuid7(\DateTimeInterface|null $dateTime = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dateTime` | **\DateTimeInterface&#124;null** | An optional date/time from which<br />to create the version 7 UUID. If not provided, the UUID is generated<br />using the current date/time. |


**Return Value:**

A UuidInterface instance that represents a
version 7 UUID




***

### uuid8

Returns a version 8 (Custom) UUID

```php
public uuid8(string $bytes): \Ramsey\Uuid\UuidInterface
```

The bytes provided may contain any value according to your application's
needs. Be aware, however, that other applications may not understand the
semantics of the value.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | A 16-byte octet string. This is an open blob<br />of data that you may fill with 128 bits of information. Be aware,<br />however, bits 48 through 51 will be replaced with the UUID version<br />field, and bits 64 and 65 will be replaced with the UUID variant. You<br />MUST NOT rely on these bits for your application needs. |


**Return Value:**

A UuidInterface instance that represents a
version 8 UUID




***

### uuid

Returns a Uuid created from the provided byte string

```php
public uuid(string $bytes): \Ramsey\Uuid\UuidInterface
```

Uses the configured builder and codec and the provided byte string to
construct a Uuid object.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | The byte string from which to construct a UUID |


**Return Value:**

An instance of UuidInterface, created from the
provided bytes




***

### uuidFromNsAndName

Returns a version 3 or 5 namespaced Uuid

```php
private uuidFromNsAndName(string|\Ramsey\Uuid\UuidInterface $ns, string $name, int $version, string $hashAlgorithm): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ns` | **string&#124;\Ramsey\Uuid\UuidInterface** | The namespace (must be a valid UUID) |
| `$name` | **string** | The name to hash together with the namespace |
| `$version` | **int** | The version of UUID to create (3 or 5) |
| `$hashAlgorithm` | **string** | The hashing algorithm to use when hashing<br />together the namespace and name |


**Return Value:**

An instance of UuidInterface, created by hashing
together the provided namespace and name




***

### uuidFromBytesAndVersion

Returns an RFC 4122 variant Uuid, created from the provided bytes and version

```php
private uuidFromBytesAndVersion(string $bytes, int $version): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | The byte string to convert to a UUID |
| `$version` | **int** | The RFC 4122 version to apply to the UUID |


**Return Value:**

An instance of UuidInterface, created from the
byte string and version




***


***
> Automatically generated on 2025-03-15
