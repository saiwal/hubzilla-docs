
# DceSecurityGenerator

DceSecurityGenerator generates strings of binary data based on a local
domain, local identifier, node ID, clock sequence, and the current time



* Full name: `\Ramsey\Uuid\Generator\DceSecurityGenerator`
* This class implements:
[`\Ramsey\Uuid\Generator\DceSecurityGeneratorInterface`](./DceSecurityGeneratorInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DOMAINS`|private| |[\Ramsey\Uuid\Uuid::DCE_DOMAIN_PERSON, \Ramsey\Uuid\Uuid::DCE_DOMAIN_GROUP, \Ramsey\Uuid\Uuid::DCE_DOMAIN_ORG]|
|`CLOCK_SEQ_HIGH`|private| |63|
|`CLOCK_SEQ_LOW`|private| |0|

## Properties


### numberConverter



```php
private \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter
```






***

### timeGenerator



```php
private \Ramsey\Uuid\Generator\TimeGeneratorInterface $timeGenerator
```






***

### dceSecurityProvider



```php
private \Ramsey\Uuid\Provider\DceSecurityProviderInterface $dceSecurityProvider
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter, \Ramsey\Uuid\Generator\TimeGeneratorInterface $timeGenerator, \Ramsey\Uuid\Provider\DceSecurityProviderInterface $dceSecurityProvider): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberConverter` | **\Ramsey\Uuid\Converter\NumberConverterInterface** |  |
| `$timeGenerator` | **\Ramsey\Uuid\Generator\TimeGeneratorInterface** |  |
| `$dceSecurityProvider` | **\Ramsey\Uuid\Provider\DceSecurityProviderInterface** |  |





***

### generate

Generate a binary string from a local domain, local identifier, node ID,
clock sequence, and current time

```php
public generate(int $localDomain, ?\Ramsey\Uuid\Type\Integer $localIdentifier = null, ?\Ramsey\Uuid\Type\Hexadecimal $node = null, ?int $clockSeq = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$localDomain` | **int** | The local domain to use when generating bytes,<br />according to DCE Security |
| `$localIdentifier` | **?\Ramsey\Uuid\Type\Integer** | The local identifier for the<br />given domain; this may be a UID or GID on POSIX systems, if the local<br />domain is person or group, or it may be a site-defined identifier<br />if the local domain is org |
| `$node` | **?\Ramsey\Uuid\Type\Hexadecimal** | A 48-bit number representing the hardware<br />address |
| `$clockSeq` | **?int** | A 14-bit number used to help avoid duplicates<br />that could arise when the clock is set backwards in time or if the<br />node ID changes |


**Return Value:**

A binary string




***


***
> Automatically generated on 2025-03-18
