***

# UnixTimeGenerator

UnixTimeGenerator generates bytes that combine a 48-bit timestamp in
milliseconds since the Unix Epoch with 80 random bits

Code and concepts within this class are borrowed from the symfony/uid package
and are used under the terms of the MIT license distributed with symfony/uid.

symfony/uid is copyright (c) Fabien Potencier.

* Full name: `\Ramsey\Uuid\Generator\UnixTimeGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\TimeGeneratorInterface`](./TimeGeneratorInterface.md)

**See Also:**

* https://symfony.com/components/Uid - Symfony Uid component
* https://github.com/symfony/uid/blob/4f9f537e57261519808a7ce1d941490736522bbc/UuidV7.php - Symfony UuidV7 class
* https://github.com/symfony/uid/blob/6.2/LICENSE - MIT License



## Properties


### time



```php
private static string $time
```



* This property is **static**.


***

### seed



```php
private static ?string $seed
```



* This property is **static**.


***

### seedIndex



```php
private static int $seedIndex
```



* This property is **static**.


***

### rand



```php
private static int[] $rand
```



* This property is **static**.


***

### seedParts



```php
private static int[] $seedParts
```



* This property is **static**.


***

### randomGenerator



```php
private \Ramsey\Uuid\Generator\RandomGeneratorInterface $randomGenerator
```






***

### intSize



```php
private int $intSize
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Generator\RandomGeneratorInterface $randomGenerator, int $intSize = PHP_INT_SIZE): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$randomGenerator` | **\Ramsey\Uuid\Generator\RandomGeneratorInterface** |  |
| `$intSize` | **int** |  |





***

### generate

Generate a binary string from a node ID, clock sequence, and current time

```php
public generate(\Ramsey\Uuid\Type\Hexadecimal|int|string|null $node = null, int|null $clockSeq = null, \DateTimeInterface $dateTime = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;int&#124;string&#124;null** | Unused in this generator |
| `$clockSeq` | **int&#124;null** | Unused in this generator |
| `$dateTime` | **\DateTimeInterface** | A date-time instance to use when<br />generating bytes |


**Return Value:**

A binary string




***

### randomize



```php
private randomize(string $time): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$time` | **string** |  |





***

### increment

Special thanks to Nicolas Grekas for sharing the following information:

```php
private increment(): string
```

Within the same ms, we increment the rand part by a random 24-bit number.

Instead of getting this number from random_bytes(), which is slow, we get
it by sha512-hashing self::$seed. This produces 64 bytes of entropy,
which we need to split in a list of 24-bit numbers. unpack() first splits
them into 16 x 32-bit numbers; we take the first byte of each of these
numbers to get 5 extra 24-bit numbers. Then, we consume those numbers
one-by-one and run this logic every 21 iterations.

self::$rand holds the random part of the UUID, split into 5 x 16-bit
numbers for x86 portability. We increment this random part by the next
24-bit number in the self::$seedParts list and decrement
self::$seedIndex.










**See Also:**

* https://twitter.com/nicolasgrekas/status/1583356938825261061 - Tweet from Nicolas Grekas

***


***
> Automatically generated on 2025-03-15
