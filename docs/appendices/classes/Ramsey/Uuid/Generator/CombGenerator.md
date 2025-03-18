
# CombGenerator

CombGenerator generates COMBs (combined UUID/timestamp)

The CombGenerator, when used with the StringCodec (and, by proxy, the
TimestampLastCombCodec) or the TimestampFirstCombCodec, combines the current
timestamp with a UUID (hence the name "COMB"). The timestamp either appears
as the first or last 48 bits of the COMB, depending on the codec used.

By default, COMBs will have the timestamp set as the last 48 bits of the
identifier.

``` php
$factory = new UuidFactory();

$factory->setRandomGenerator(new CombGenerator(
    $factory->getRandomGenerator(),
    $factory->getNumberConverter()
));

$comb = $factory->uuid4();
```

To generate a COMB with the timestamp as the first 48 bits, set the
TimestampFirstCombCodec as the codec.

``` php
$factory->setCodec(new TimestampFirstCombCodec($factory->getUuidBuilder()));
```

* Full name: `\Ramsey\Uuid\Generator\CombGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\RandomGeneratorInterface`](./RandomGeneratorInterface.md)

**See Also:**

* https://www.informit.com/articles/printerfriendly/25862 - The Cost of GUIDs as Primary Keys


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TIMESTAMP_BYTES`|public| |6|

## Properties


### generator



```php
private \Ramsey\Uuid\Generator\RandomGeneratorInterface $generator
```






***

### numberConverter



```php
private \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Generator\RandomGeneratorInterface $generator, \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$generator` | **\Ramsey\Uuid\Generator\RandomGeneratorInterface** |  |
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** |  |





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



**Throws:**
<p>if $length is not a positive integer
greater than or equal to CombGenerator::TIMESTAMP_BYTES</p>

- [`InvalidArgumentException`](../Exception/InvalidArgumentException.md)



***

### timestamp

Returns current timestamp a string integer, precise to 0.00001 seconds

```php
private timestamp(): string
```












***


***
> Automatically generated on 2025-03-18
