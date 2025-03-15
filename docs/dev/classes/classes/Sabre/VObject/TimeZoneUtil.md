
# TimeZoneUtil

Time zone name translation.

This file translates well-known time zone names into "Olson database" time zone names.

* Full name: `\Sabre\VObject\TimeZoneUtil`



## Properties


### instance



```php
private static self $instance
```



* This property is **static**.


***

### timezoneGuessers



```php
private \Sabre\VObject\TimezoneGuesser\TimezoneGuesser[] $timezoneGuessers
```






***

### timezoneFinders



```php
private \Sabre\VObject\TimezoneGuesser\TimezoneFinder[] $timezoneFinders
```






***

### map



```php
public static array|null $map
```



* This property is **static**.
* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### microsoftExchangeMap

List of microsoft exchange timezone ids.

```php
public static $microsoftExchangeMap
```

Source: http://msdn.microsoft.com/en-us/library/aa563018(loband).aspx

* This property is **static**.
* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

## Methods


### __construct



```php
private __construct(): mixed
```












***

### getInstance



```php
private static getInstance(): self
```



* This method is **static**.








***

### addGuesser



```php
private addGuesser(string $key, \Sabre\VObject\TimezoneGuesser\TimezoneGuesser $guesser): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$guesser` | **\Sabre\VObject\TimezoneGuesser\TimezoneGuesser** |  |





***

### addFinder



```php
private addFinder(string $key, \Sabre\VObject\TimezoneGuesser\TimezoneFinder $finder): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$finder` | **\Sabre\VObject\TimezoneGuesser\TimezoneFinder** |  |





***

### findTimeZone

This method will try to find out the correct timezone for an iCalendar
date-time value.

```php
private findTimeZone(string $tzid, \Sabre\VObject\Component $vcalendar = null, bool $failIfUncertain = false): \DateTimeZone
```

You must pass the contents of the TZID parameter, as well as the full
calendar.

If the lookup fails, this method will return the default PHP timezone
(as configured using date_default_timezone_set, or the date.timezone ini
setting).

Alternatively, if $failIfUncertain is set to true, it will throw an
exception if we cannot accurately determine the timezone.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tzid` | **string** |  |
| `$vcalendar` | **\Sabre\VObject\Component** |  |
| `$failIfUncertain` | **bool** |  |





***

### addTimezoneGuesser



```php
public static addTimezoneGuesser(string $key, \Sabre\VObject\TimezoneGuesser\TimezoneGuesser $guesser): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$guesser` | **\Sabre\VObject\TimezoneGuesser\TimezoneGuesser** |  |





***

### addTimezoneFinder



```php
public static addTimezoneFinder(string $key, \Sabre\VObject\TimezoneGuesser\TimezoneFinder $finder): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$finder` | **\Sabre\VObject\TimezoneGuesser\TimezoneFinder** |  |





***

### getTimeZone



```php
public static getTimeZone(string $tzid, \Sabre\VObject\Component $vcalendar = null, false $failIfUncertain = false): \DateTimeZone
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tzid` | **string** |  |
| `$vcalendar` | **\Sabre\VObject\Component** |  |
| `$failIfUncertain` | **false** |  |





***

### clean



```php
public static clean(): void
```



* This method is **static**.








***

### loadTzMaps

This method will load in all the tz mapping information, if it's not yet
done.

```php
public static loadTzMaps(): mixed
```



* This method is **static**.


* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getIdentifiersBC

This method returns an array of timezone identifiers, that are supported
by DateTimeZone(), but not returned by DateTimeZone::listIdentifiers().

```php
public static getIdentifiersBC(): array
```

We're not using DateTimeZone::listIdentifiers(DateTimeZone::ALL_WITH_BC) because:
- It's not supported by some PHP versions as well as HHVM.
- It also returns identifiers, that are invalid values for new DateTimeZone() on some PHP versions.
(See timezonedata/php-bc.php and timezonedata php-workaround.php)

* This method is **static**.


* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***


***
> Automatically generated on 2025-03-15
