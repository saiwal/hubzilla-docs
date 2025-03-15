***

# FindFromTimezoneMap

Some clients add 'X-LIC-LOCATION' with the olson name.



* Full name: `\Sabre\VObject\TimezoneGuesser\FindFromTimezoneMap`
* This class implements:
[`\Sabre\VObject\TimezoneGuesser\TimezoneFinder`](./TimezoneFinder.md)



## Properties


### map



```php
private $map
```






***

### patterns



```php
private $patterns
```






***

## Methods


### find



```php
public find(string $tzid, bool $failIfUncertain = false): ?\DateTimeZone
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tzid` | **string** |  |
| `$failIfUncertain` | **bool** |  |





***

### getTzMaps

This method returns an array of timezone identifiers, that are supported
by DateTimeZone(), but not returned by DateTimeZone::listIdentifiers().

```php
private getTzMaps(): array
```

We're not using DateTimeZone::listIdentifiers(DateTimeZone::ALL_WITH_BC) because:
- It's not supported by some PHP versions as well as HHVM.
- It also returns identifiers, that are invalid values for new DateTimeZone() on some PHP versions.
(See timezonedata/php-bc.php and timezonedata php-workaround.php)










***

### getTzFromMap



```php
private getTzFromMap(string $tzid): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tzid` | **string** |  |





***

### hasTzInMap



```php
private hasTzInMap(string $tzid): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tzid` | **string** |  |





***


***
> Automatically generated on 2025-03-15
