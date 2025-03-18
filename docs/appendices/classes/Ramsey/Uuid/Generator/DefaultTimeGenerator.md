
# DefaultTimeGenerator

DefaultTimeGenerator generates strings of binary data based on a node ID,
clock sequence, and the current time



* Full name: `\Ramsey\Uuid\Generator\DefaultTimeGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\TimeGeneratorInterface`](./TimeGeneratorInterface.md)



## Properties


### nodeProvider



```php
private \Ramsey\Uuid\Provider\NodeProviderInterface $nodeProvider
```






***

### timeConverter



```php
private \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter
```






***

### timeProvider



```php
private \Ramsey\Uuid\Provider\TimeProviderInterface $timeProvider
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Provider\NodeProviderInterface $nodeProvider, \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter, \Ramsey\Uuid\Provider\TimeProviderInterface $timeProvider): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$nodeProvider` | **\Ramsey\Uuid\Provider\NodeProviderInterface** |  |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface** |  |
| `$timeProvider` | **\Ramsey\Uuid\Provider\TimeProviderInterface** |  |





***

### generate

Generate a binary string from a node ID, clock sequence, and current time

```php
public generate(mixed $node = null, ?int $clockSeq = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **mixed** | A 48-bit number representing the<br />hardware address; this number may be represented as an integer or a<br />hexadecimal string |
| `$clockSeq` | **?int** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A binary string



**Throws:**
<p>if the parameters contain invalid values</p>

- [`InvalidArgumentException`](../Exception/InvalidArgumentException.md)
<p>if random_int() throws an exception/error</p>

- [`RandomSourceException`](../Exception/RandomSourceException.md)



***

### getValidNode

Uses the node provider given when constructing this instance to get
the node ID (usually a MAC address)

```php
private getValidNode(int|string|null $node): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **int&#124;string&#124;null** | A node value that may be used to override the node provider |


**Return Value:**

6-byte binary string representation of the node



**Throws:**

- [`InvalidArgumentException`](../Exception/InvalidArgumentException.md)



***


***
> Automatically generated on 2025-03-18
