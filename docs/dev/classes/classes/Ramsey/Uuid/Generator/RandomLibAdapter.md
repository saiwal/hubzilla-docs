***

# RandomLibAdapter

RandomLibAdapter generates strings of random binary data using the
paragonie/random-lib library



* Full name: `\Ramsey\Uuid\Generator\RandomLibAdapter`
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.
* This class implements:
[`\Ramsey\Uuid\Generator\RandomGeneratorInterface`](./RandomGeneratorInterface.md)

**See Also:**

* https://packagist.org/packages/paragonie/random-lib - paragonie/random-lib



## Properties


### generator



```php
private \RandomLib\Generator $generator
```






***

## Methods


### __construct

Constructs a RandomLibAdapter

```php
public __construct(\RandomLib\Generator|null $generator = null): mixed
```

By default, if no Generator is passed in, this creates a high-strength
generator to use when generating random binary data.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$generator` | **\RandomLib\Generator&#124;null** | The generator to use when generating binary data |





***

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




***


***
> Automatically generated on 2025-03-15
