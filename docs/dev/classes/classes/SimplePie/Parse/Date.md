
# Date

Date Parser



* Full name: `\SimplePie\Parse\Date`



## Properties


### date

Input data

```php
public string $date
```






***

### day

List of days, calendar day name => ordinal day number in the week

```php
public array $day
```






***

### month

List of months, calendar month name => calendar month number

```php
public array $month
```






***

### timezone

List of timezones, abbreviation => offset from UTC

```php
public array $timezone
```






***

### day_pcre

Cached PCRE for Date::$day

```php
public string $day_pcre
```






***

### month_pcre

Cached PCRE for Date::$month

```php
public string $month_pcre
```






***

### built_in

Array of user-added callback methods

```php
public array $built_in
```






***

### user

Array of user-added callback methods

```php
public array $user
```






***

## Methods


### __construct

Create new Date object, and set self::day_pcre,
self::month_pcre, and self::built_in

```php
public __construct(): mixed
```












***

### get

Get the object

```php
public static get(): mixed
```



* This method is **static**.








***

### parse

Parse a date

```php
public parse(string $date): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** | Date to parse |


**Return Value:**

Timestamp corresponding to date string, or false on failure




***

### add_callback

Add a callback method to parse a date

```php
public add_callback(callable $callback): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$callback` | **callable** |  |





***

### date_w3cdtf

Parse a superset of W3C-DTF (allows hyphens and colons to be omitted, as
well as allowing any of upper or lower case "T", horizontal tabs, or
spaces to be used as the time separator (including more than one))

```php
public date_w3cdtf(mixed $date): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **mixed** |  |


**Return Value:**

Timestamp




***

### remove_rfc2822_comments

Remove RFC822 comments

```php
public remove_rfc2822_comments(mixed $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |


**Return Value:**

Comment stripped string




***

### date_rfc2822

Parse RFC2822's date format

```php
public date_rfc2822(mixed $date): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **mixed** |  |


**Return Value:**

Timestamp




***

### date_rfc850

Parse RFC850's date format

```php
public date_rfc850(mixed $date): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **mixed** |  |


**Return Value:**

Timestamp




***

### date_asctime

Parse C99's asctime()'s date format

```php
public date_asctime(mixed $date): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **mixed** |  |


**Return Value:**

Timestamp




***

### date_strtotime

Parse dates using strtotime()

```php
public date_strtotime(mixed $date): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **mixed** |  |


**Return Value:**

Timestamp




***


***
> Automatically generated on 2025-03-15
