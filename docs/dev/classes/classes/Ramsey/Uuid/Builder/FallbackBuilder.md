
# FallbackBuilder

FallbackBuilder builds a UUID by stepping through a list of UUID builders
until a UUID can be constructed without exceptions



* Full name: `\Ramsey\Uuid\Builder\FallbackBuilder`
* This class implements:
[`\Ramsey\Uuid\Builder\UuidBuilderInterface`](./UuidBuilderInterface.md)



## Properties


### builders



```php
private iterable $builders
```






***

## Methods


### __construct



```php
public __construct(iterable&lt;\Ramsey\Uuid\Builder\UuidBuilderInterface&gt; $builders): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$builders` | **iterable<\Ramsey\Uuid\Builder\UuidBuilderInterface>** | An array of UUID builders |





***

### build

Builds and returns a UuidInterface instance using the first builder that
succeeds

```php
public build(\Ramsey\Uuid\Codec\CodecInterface $codec, string $bytes): \Ramsey\Uuid\UuidInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codec` | **\Ramsey\Uuid\Codec\CodecInterface** | The codec to use for building this instance |
| `$bytes` | **string** | The byte string from which to construct a UUID |


**Return Value:**

an instance of a UUID object




***


***
> Automatically generated on 2025-03-15
