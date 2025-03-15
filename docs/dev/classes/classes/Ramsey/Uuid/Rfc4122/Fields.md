
# Fields

RFC 4122 variant UUIDs are comprised of a set of named fields

Internally, this class represents the fields together as a 16-byte binary
string.

* Full name: `\Ramsey\Uuid\Rfc4122\Fields`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\Ramsey\Uuid\Rfc4122\FieldsInterface`](./FieldsInterface.md)
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
<p>if the byte string does not represent an RFC 4122 UUID</p>

- [`InvalidArgumentException`](../Exception/InvalidArgumentException.md)
<p>if the byte string does not contain a valid version</p>

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

For version 2 UUIDs, the time_low field is the local identifier and
should not be returned as part of the time. For this reason, we set the
bottom 32 bits of the timestamp to 0's. As a result, there is some loss
of fidelity of the timestamp, for version 2 UUIDs. The timestamp can be
off by a range of 0 to 429.4967295 seconds (or 7 minutes, 9 seconds, and
496730 microseconds).

For version 6 UUIDs, the timestamp order is reversed from the typical RFC
4122 order (the time bits are in the correct bit order, so that it is
monotonically increasing). In returning the timestamp value, we put the
bits in the order: time_low + time_mid + time_hi.










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

### isCorrectVariant



```php
private isCorrectVariant(): bool
```












***


## Inherited methods


### getVersion

Returns the version

```php
public getVersion(): ?int
```




* This method is **abstract**.







***

### isMax

Returns true if the byte string represents a max UUID

```php
public isMax(): bool
```












***

### isNil

Returns true if the byte string represents a nil UUID

```php
public isNil(): bool
```












***

### isCorrectVersion

Returns true if the version matches one of those defined by RFC 4122

```php
private isCorrectVersion(): bool
```









**Return Value:**

True if the UUID version is valid, false otherwise




***

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
