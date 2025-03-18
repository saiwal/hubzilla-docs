
# FindFromTimezoneIdentifier

Some clients add 'X-LIC-LOCATION' with the olson name.



* Full name: `\Sabre\VObject\TimezoneGuesser\FindFromTimezoneIdentifier`
* This class implements:
[`\Sabre\VObject\TimezoneGuesser\TimezoneFinder`](./TimezoneFinder.md)




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

### getIdentifiersBC

This method returns an array of timezone identifiers, that are supported
by DateTimeZone(), but not returned by DateTimeZone::listIdentifiers().

```php
private getIdentifiersBC(): array
```

We're not using DateTimeZone::listIdentifiers(DateTimeZone::ALL_WITH_BC) because:
- It's not supported by some PHP versions as well as HHVM.
- It also returns identifiers, that are invalid values for new DateTimeZone() on some PHP versions.
(See timezonedata/php-bc.php and timezonedata php-workaround.php)










***


***
> Automatically generated on 2025-03-18
