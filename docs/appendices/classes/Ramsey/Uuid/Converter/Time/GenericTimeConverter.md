
# GenericTimeConverter

GenericTimeConverter uses the provided calculator to calculate and convert
time values



* Full name: `\Ramsey\Uuid\Converter\Time\GenericTimeConverter`
* This class implements:
[`\Ramsey\Uuid\Converter\TimeConverterInterface`](../TimeConverterInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`GREGORIAN_TO_UNIX_INTERVALS`|private| |&#039;122192928000000000&#039;|
|`SECOND_INTERVALS`|private| |&#039;10000000&#039;|
|`MICROSECOND_INTERVALS`|private| |&#039;10&#039;|

## Properties


### calculator



```php
private \Ramsey\Uuid\Math\CalculatorInterface $calculator
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Math\CalculatorInterface $calculator): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calculator` | **\Ramsey\Uuid\Math\CalculatorInterface** |  |





***

### calculateTime

Uses the provided seconds and micro-seconds to calculate the count of
100-nanosecond intervals since UTC 00:00:00.00, 15 October 1582, for
RFC 4122 variant UUIDs

```php
public calculateTime(string $seconds, string $microseconds): \Ramsey\Uuid\Type\Hexadecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$seconds` | **string** | A string representation of the number of seconds<br />since the Unix epoch for the time to calculate |
| `$microseconds` | **string** | A string representation of the micro-seconds<br />associated with the time to calculate |


**Return Value:**

The full UUID timestamp as a Hexadecimal value




***

### convertTime

Converts a timestamp extracted from a UUID to a Unix timestamp

```php
public convertTime(\Ramsey\Uuid\Type\Hexadecimal $uuidTimestamp): \Ramsey\Uuid\Type\Time
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuidTimestamp` | **\Ramsey\Uuid\Type\Hexadecimal** | A hexadecimal representation of a UUID<br />timestamp; a UUID timestamp is a count of 100-nanosecond intervals<br />since UTC 00:00:00.00, 15 October 1582. |


**Return Value:**

An instance of {@see \Ramsey\Uuid\Type\Time}




***


***
> Automatically generated on 2025-03-18
