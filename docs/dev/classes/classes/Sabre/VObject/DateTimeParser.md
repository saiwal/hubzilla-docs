***

# DateTimeParser

DateTimeParser.

This class is responsible for parsing the several different date and time
formats iCalendar and vCards have.

* Full name: `\Sabre\VObject\DateTimeParser`




## Methods


### parseDateTime

Parses an iCalendar (rfc5545) formatted datetime and returns a
DateTimeImmutable object.

```php
public static parseDateTime(string $dt, \DateTimeZone $tz = null): \DateTimeImmutable
```

Specifying a reference timezone is optional. It will only be used
if the non-UTC format is used. The argument is used as a reference, the
returned DateTimeImmutable object will still be in the UTC timezone.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dt` | **string** |  |
| `$tz` | **\DateTimeZone** |  |





***

### parseDate

Parses an iCalendar (rfc5545) formatted date and returns a DateTimeImmutable object.

```php
public static parseDate(string $date, \DateTimeZone $tz = null): \DateTimeImmutable
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** |  |
| `$tz` | **\DateTimeZone** |  |





***

### parseDuration

Parses an iCalendar (RFC5545) formatted duration value.

```php
public static parseDuration(string $duration, bool $asString = false): \DateInterval|string
```

This method will either return a DateTimeInterval object, or a string
suitable for strtotime or DateTime::modify.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$duration` | **string** |  |
| `$asString` | **bool** |  |





***

### parse

Parses either a Date or DateTime, or Duration value.

```php
public static parse(string $date, \DateTimeZone|string $referenceTz = null): \DateTimeImmutable|\DateInterval
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** |  |
| `$referenceTz` | **\DateTimeZone&#124;string** |  |





***

### parseVCardDateTime

This method parses a vCard date and or time value.

```php
public static parseVCardDateTime(string $date): array
```

This can be used for the DATE, DATE-TIME, TIMESTAMP and
DATE-AND-OR-TIME value.

This method returns an array, not a DateTime value.

The elements in the array are in the following order:
year, month, date, hour, minute, second, timezone

Almost any part of the string may be omitted. It's for example legal to
just specify seconds, leave out the year, etc.

Timezone is either returned as 'Z' or as '+0800'

For any non-specified values null is returned.

List of date formats that are supported:
YYYY
YYYY-MM
YYYYMMDD
--MMDD
---DD

YYYY-MM-DD
--MM-DD
---DD

List of supported time formats:

HH
HHMM
HHMMSS
-MMSS
--SS

HH
HH:MM
HH:MM:SS
-MM:SS
--SS

A full basic-format date-time string looks like :
20130603T133901

A full extended-format date-time string looks like :
2013-06-03T13:39:01

Times may be postfixed by a timezone offset. This can be either 'Z' for
UTC, or a string like -0500 or +1100.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** |  |





***

### parseVCardTime

This method parses a vCard TIME value.

```php
public static parseVCardTime(string $date): array
```

This method returns an array, not a DateTime value.

The elements in the array are in the following order:
hour, minute, second, timezone

Almost any part of the string may be omitted. It's for example legal to
just specify seconds, leave out the hour etc.

Timezone is either returned as 'Z' or as '+08:00'

For any non-specified values null is returned.

List of supported time formats:

HH
HHMM
HHMMSS
-MMSS
--SS

HH
HH:MM
HH:MM:SS
-MM:SS
--SS

A full basic-format time string looks like :
133901

A full extended-format time string looks like :
13:39:01

Times may be postfixed by a timezone offset. This can be either 'Z' for
UTC, or a string like -0500 or +11:00.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** |  |





***

### parseVCardDateAndOrTime

This method parses a vCard date and or time value.

```php
public static parseVCardDateAndOrTime(string $date): array
```

This can be used for the DATE, DATE-TIME and
DATE-AND-OR-TIME value.

This method returns an array, not a DateTime value.
The elements in the array are in the following order:
    year, month, date, hour, minute, second, timezone
Almost any part of the string may be omitted. It's for example legal to
just specify seconds, leave out the year, etc.

Timezone is either returned as 'Z' or as '+0800'

For any non-specified values null is returned.

List of date formats that are supported:
    20150128
    2015-01
    --01
    --0128
    ---28

List of supported time formats:
    13
    1353
    135301
    -53
    -5301
    --01 (unreachable, see the tests)
    --01Z
    --01+1234

List of supported date-time formats:
    20150128T13
    --0128T13
    ---28T13
    ---28T1353
    ---28T135301
    ---28T13Z
    ---28T13+1234

See the regular expressions for all the possible patterns.

Times may be postfixed by a timezone offset. This can be either 'Z' for
UTC, or a string like -0500 or +1100.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** |  |





***


***
> Automatically generated on 2025-03-15
