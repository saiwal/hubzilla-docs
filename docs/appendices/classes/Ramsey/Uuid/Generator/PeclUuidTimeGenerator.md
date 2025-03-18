
# PeclUuidTimeGenerator

PeclUuidTimeGenerator generates strings of binary data for time-base UUIDs,
using ext-uuid



* Full name: `\Ramsey\Uuid\Generator\PeclUuidTimeGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\TimeGeneratorInterface`](./TimeGeneratorInterface.md)

**See Also:**

* https://pecl.php.net/package/uuid - ext-uuid




## Methods


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




***


***
> Automatically generated on 2025-03-18
