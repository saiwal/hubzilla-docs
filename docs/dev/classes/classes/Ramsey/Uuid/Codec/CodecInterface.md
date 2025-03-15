***

# CodecInterface

A codec encodes and decodes a UUID according to defined rules



* Full name: `\Ramsey\Uuid\Codec\CodecInterface`



## Methods


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


***
> Automatically generated on 2025-03-15
