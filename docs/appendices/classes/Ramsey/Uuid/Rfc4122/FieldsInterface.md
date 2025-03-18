
# FieldsInterface

RFC 4122 defines fields for a specific variant of UUID

The fields of an RFC 4122 variant UUID are:

* **time_low**: The low field of the timestamp, an unsigned 32-bit integer
* **time_mid**: The middle field of the timestamp, an unsigned 16-bit integer
* **time_hi_and_version**: The high field of the timestamp multiplexed with
  the version number, an unsigned 16-bit integer
* **clock_seq_hi_and_reserved**: The high field of the clock sequence
  multiplexed with the variant, an unsigned 8-bit integer
* **clock_seq_low**: The low field of the clock sequence, an unsigned
  8-bit integer
* **node**: The spatially unique node identifier, an unsigned 48-bit
  integer

* Full name: `\Ramsey\Uuid\Rfc4122\FieldsInterface`
* Parent interfaces: [`\Ramsey\Uuid\Fields\FieldsInterface`](../Fields/FieldsInterface.md)
**See Also:**

* http://tools.ietf.org/html/rfc4122#section-4.1 - RFC 4122, § 4.1: Format



## Methods


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

### getVariant

Returns the variant

```php
public getVariant(): int
```

The variant number describes the layout of the UUID. The variant
number has the following meaning:

- 0 - Reserved for NCS backward compatibility
- 2 - The RFC 4122 variant
- 6 - Reserved, Microsoft Corporation backward compatibility
- 7 - Reserved for future definition

For RFC 4122 variant UUIDs, this value should always be the integer `2`.










**See Also:**

* http://tools.ietf.org/html/rfc4122#section-4.1.1 - RFC 4122, § 4.1.1: Variant

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










**See Also:**

* http://tools.ietf.org/html/rfc4122#section-4.1.3 - RFC 4122, § 4.1.3: Version

***

### isNil

Returns true if these fields represent a nil UUID

```php
public isNil(): bool
```

The nil UUID is special form of UUID that is specified to have all 128
bits set to zero.










***


## Inherited methods


### getBytes

Returns the bytes that comprise the fields

```php
public getBytes(): string
```












***


***
> Automatically generated on 2025-03-18
