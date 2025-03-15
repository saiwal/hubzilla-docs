
# OrderedTimeCodec

OrderedTimeCodec encodes and decodes a UUID, optimizing the byte order for
more efficient storage

For binary representations of version 1 UUID, this codec may be used to
reorganize the time fields, making the UUID closer to sequential when storing
the bytes. According to Percona, this optimization can improve database
INSERTs and SELECTs using the UUID column as a key.

The string representation of the UUID will remain unchanged. Only the binary
representation is reordered.

**PLEASE NOTE:** Binary representations of UUIDs encoded with this codec must
be decoded with this codec. Decoding using another codec can result in
malformed UUIDs.

* Full name: `\Ramsey\Uuid\Codec\OrderedTimeCodec`
* Parent class: [`\Ramsey\Uuid\Codec\StringCodec`](./StringCodec.md)

**See Also:**

* https://www.percona.com/blog/2014/12/19/store-uuid-optimized-way/ - Storing UUID Values in MySQL




## Methods


### encodeBinary

Returns a binary string representation of a UUID, with the timestamp
fields rearranged for optimized storage

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

### decodeBytes

Returns a UuidInterface derived from an ordered-time binary string
representation

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



**Throws:**
<p>if $bytes is an invalid length</p>

- [`InvalidArgumentException`](../Exception/InvalidArgumentException.md)



***


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
