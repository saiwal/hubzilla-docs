***

# PeclUuidNameGenerator

PeclUuidNameGenerator generates strings of binary data from a namespace and a
name, using ext-uuid



* Full name: `\Ramsey\Uuid\Generator\PeclUuidNameGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\NameGeneratorInterface`](./NameGeneratorInterface.md)

**See Also:**

* https://pecl.php.net/package/uuid - ext-uuid




## Methods


### generate

Generate a binary string from a namespace and name hashed together with
the specified hashing algorithm

```php
public generate(\Ramsey\Uuid\UuidInterface $ns, string $name, string $hashAlgorithm): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ns` | **\Ramsey\Uuid\UuidInterface** | The namespace |
| `$name` | **string** | The name to use for creating a UUID |
| `$hashAlgorithm` | **string** | The hashing algorithm to use |


**Return Value:**

A binary string




***


***
> Automatically generated on 2025-03-15
