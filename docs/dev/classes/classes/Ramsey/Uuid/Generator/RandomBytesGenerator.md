
# RandomBytesGenerator

RandomBytesGenerator generates strings of random binary data using the
built-in `random_bytes()` PHP function



* Full name: `\Ramsey\Uuid\Generator\RandomBytesGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\RandomGeneratorInterface`](./RandomGeneratorInterface.md)

**See Also:**

* http://php.net/random_bytes - random_bytes()




## Methods


### generate

Generates a string of randomized binary data

```php
public generate(int $length): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** | The number of bytes of random binary data to generate |


**Return Value:**

A binary string



**Throws:**
<p>if random_bytes() throws an exception/error</p>

- [`RandomSourceException`](../Exception/RandomSourceException.md)



***


***
> Automatically generated on 2025-03-15
