
# UuidFactoryInterface

UuidFactoryInterface defines common functionality all `UuidFactory` instances
must implement



* Full name: `\Ramsey\Uuid\UuidFactoryInterface`



## Methods


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

### fromDateTime

Creates a UUID from a DateTimeInterface instance

```php
public fromDateTime(\DateTimeInterface $dateTime, \Ramsey\Uuid\Type\Hexadecimal|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








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

### getValidator

Returns the validator to use for the factory

```php
public getValidator(): \Ramsey\Uuid\Validator\ValidatorInterface
```












***

### uuid1

Returns a version 1 (Gregorian time) UUID from a host ID, sequence number,
and the current time

```php
public uuid1(\Ramsey\Uuid\Type\Hexadecimal|int|string|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;int&#124;string&#124;null** | A 48-bit number representing the<br />hardware address; this number may be represented as an integer or a<br />hexadecimal string |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 1 UUID




***

### uuid2

Returns a version 2 (DCE Security) UUID from a local domain, local
identifier, host ID, clock sequence, and the current time

```php
public uuid2(int $localDomain, \Ramsey\Uuid\Type\Integer|null $localIdentifier = null, \Ramsey\Uuid\Type\Hexadecimal|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$localDomain` | **int** | The local domain to use when generating bytes,<br />according to DCE Security |
| `$localIdentifier` | **\Ramsey\Uuid\Type\Integer&#124;null** | The local identifier for the<br />given domain; this may be a UID or GID on POSIX systems, if the local<br />domain is person or group, or it may be a site-defined identifier<br />if the local domain is org |
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;null** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 2 UUID




***

### uuid3

Returns a version 3 (name-based) UUID based on the MD5 hash of a
namespace ID and a name

```php
public uuid3(string|\Ramsey\Uuid\UuidInterface $ns, string $name): \Ramsey\Uuid\UuidInterface
```








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
public uuid5(string|\Ramsey\Uuid\UuidInterface $ns, string $name): \Ramsey\Uuid\UuidInterface
```








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
public uuid6(\Ramsey\Uuid\Type\Hexadecimal|null $node = null, int|null $clockSeq = null): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;null** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A UuidInterface instance that represents a
version 6 UUID




***


***
> Automatically generated on 2025-03-15
