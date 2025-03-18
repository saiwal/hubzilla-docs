
# TimeConverterInterface

A time converter converts timestamps into representations that may be used
in UUIDs



* Full name: `\Ramsey\Uuid\Converter\TimeConverterInterface`



## Methods


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




**See Also:**

* http://tools.ietf.org/html/rfc4122#section-4.2.2 - RFC 4122, § 4.2.2: Generation Details

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
