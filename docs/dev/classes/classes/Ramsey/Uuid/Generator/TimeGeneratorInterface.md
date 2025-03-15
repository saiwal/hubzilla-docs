***

# TimeGeneratorInterface

A time generator generates strings of binary data based on a node ID,
clock sequence, and the current time



* Full name: `\Ramsey\Uuid\Generator\TimeGeneratorInterface`



## Methods


### generate

Generate a binary string from a node ID, clock sequence, and current time

```php
public generate(\Ramsey\Uuid\Type\Hexadecimal|int|string|null $node = null, int|null $clockSeq = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;int&#124;string&#124;null** | A 48-bit number representing the<br />hardware address; this number may be represented as an integer or a<br />hexadecimal string |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A binary string




***


***
> Automatically generated on 2025-03-15
