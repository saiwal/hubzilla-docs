
# DceSecurityGeneratorInterface

A DCE Security generator generates strings of binary data based on a local
domain, local identifier, node ID, clock sequence, and the current time



* Full name: `\Ramsey\Uuid\Generator\DceSecurityGeneratorInterface`

**See Also:**

* \Ramsey\Uuid\Rfc4122\UuidV2 - 



## Methods


### generate

Generate a binary string from a local domain, local identifier, node ID,
clock sequence, and current time

```php
public generate(int $localDomain, \Ramsey\Uuid\Type\Integer|null $localIdentifier = null, \Ramsey\Uuid\Type\Hexadecimal|null $node = null, int|null $clockSeq = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$localDomain` | **int** | The local domain to use when generating bytes,<br />according to DCE Security |
| `$localIdentifier` | **\Ramsey\Uuid\Type\Integer&#124;null** | The local identifier for the<br />given domain; this may be a UID or GID on POSIX systems, if the local<br />domain is person or group, or it may be a site-defined identifier<br />if the local domain is org |
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal&#124;null** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **int&#124;null** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A binary string




***


***
> Automatically generated on 2025-03-15
