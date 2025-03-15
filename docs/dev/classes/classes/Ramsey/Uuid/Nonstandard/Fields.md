
# Fields

Nonstandard UUID fields do not conform to the RFC 4122 standard

Since some systems may create nonstandard UUIDs, this implements the
Rfc4122\FieldsInterface, so that functionality of a nonstandard UUID is not
degraded, in the event these UUIDs are expected to contain RFC 4122 fields.

Internally, this class represents the fields together as a 16-byte binary
string.

* Full name: `\Ramsey\Uuid\Nonstandard\Fields`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\Ramsey\Uuid\Rfc4122\FieldsInterface`](../Rfc4122/FieldsInterface.md)
* This class is a **Final class**



## Properties


### bytes



```php
private string $bytes
```






***

## Methods


### __construct



```php
public __construct(string $bytes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | A 16-byte binary string representation of a UUID |




**Throws:**
<p>if the byte string is not exactly 16 bytes</p>

- [`InvalidArgumentException`](../Exception/InvalidArgumentException.md)



***

### getBytes

Returns the bytes that comprise the fields

```php
public getBytes(): string
```












***

### getClockSeq

Returns the full 16-bit clock sequence, with the variant bits (two most
significant bits) masked out

```php
public getClockSeq(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getClockSeqHiAndReserved

Returns the high field of the clock sequence multiplexed with the variant

```php
public getClockSeqHiAndReserved(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getClockSeqLow

Returns the low field of the clock sequence

```php
public getClockSeqLow(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getNode

Returns the node field

```php
public getNode(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getTimeHiAndVersion

Returns the high field of the timestamp multiplexed with the version

```php
public getTimeHiAndVersion(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getTimeLow

Returns the low field of the timestamp

```php
public getTimeLow(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getTimeMid

Returns the middle field of the timestamp

```php
public getTimeMid(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getTimestamp

Returns the full 60-bit timestamp, without the version

```php
public getTimestamp(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getVersion

Returns the version

```php
public getVersion(): ?int
```

The version number describes how the UUID was generated and has the
following meaning:

1. Gregorian time UUID
2. DCE security UUID
3. Name-based UUID hashed with MD5
4. Randomly generated UUID
5. Name-based UUID hashed with SHA-1
6. Reordered time UUID
7. Unix Epoch time UUID

This returns `null` if the UUID is not an RFC 4122 variant, since version
is only meaningful for this variant.










***

### isNil

Returns true if these fields represent a nil UUID

```php
public isNil(): bool
```

The nil UUID is special form of UUID that is specified to have all 128
bits set to zero.










***

### isMax



```php
public isMax(): bool
```












***


## Inherited methods


### getBytes

Returns the bytes that comprise the fields

```php
public getBytes(): string
```




* This method is **abstract**.







***

### getVariant

Returns the variant identifier, according to RFC 4122, for the given bytes

```php
public getVariant(): int
```

The following values may be returned:

- `0` -- Reserved, NCS backward compatibility.
- `2` -- The variant specified in RFC 4122.
- `6` -- Reserved, Microsoft Corporation backward compatibility.
- `7` -- Reserved for future definition.







**Return Value:**

The variant identifier, according to RFC 4122




**See Also:**

* https://tools.ietf.org/html/rfc4122#section-4.1.1 - RFC 4122, § 4.1.1: Variant

***

### __construct



```php
public __construct(string $bytes): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | The bytes that comprise the fields |





***

### serialize

Returns a string representation of object

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
public __unserialize(array{bytes?: string} $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array{bytes?: string}** |  |





***


***
> Automatically generated on 2025-03-15
