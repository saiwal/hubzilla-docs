***

# DegradedTimeConverter

Previously used to integrate moontoast/math as a bignum arithmetic library,
BigNumberTimeConverter is deprecated in favor of GenericTimeConverter



* Full name: `\Ramsey\Uuid\Converter\Time\DegradedTimeConverter`
* Parent class: [`\Ramsey\Uuid\Converter\Time\BigNumberTimeConverter`](./BigNumberTimeConverter.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct



```php
public __construct(): mixed
```












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
> Automatically generated on 2025-03-15
