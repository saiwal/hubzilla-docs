
# DefaultNameGenerator

DefaultNameGenerator generates strings of binary data based on a namespace,
name, and hashing algorithm



* Full name: `\Ramsey\Uuid\Generator\DefaultNameGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\NameGeneratorInterface`](./NameGeneratorInterface.md)




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
> Automatically generated on 2025-03-18
