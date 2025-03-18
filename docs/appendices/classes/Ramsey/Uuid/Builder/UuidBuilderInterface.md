
# UuidBuilderInterface

A UUID builder builds instances of UuidInterface



* Full name: `\Ramsey\Uuid\Builder\UuidBuilderInterface`



## Methods


### build

Builds and returns a UuidInterface

```php
public build(\Ramsey\Uuid\Codec\CodecInterface $codec, string $bytes): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use for building this UuidInterface instance |
| `$bytes` | **string** | The byte string from which to construct a UUID |


**Return Value:**

Implementations may choose to return more specific
instances of UUIDs that implement UuidInterface




***


***
> Automatically generated on 2025-03-18
