
# StringUtil

String utility.

This class is mainly used to implement the 'text-match' filter, used by both
the CalDAV calendar-query REPORT, and CardDAV addressbook-query REPORT.
Because they both need it, it was decided to put it in Sabre\DAV instead.

* Full name: `\Sabre\DAV\StringUtil`




## Methods


### textMatch

Checks if a needle occurs in a haystack ;).

```php
public static textMatch(string $haystack, string $needle, string $collation, string $matchType = &#039;contains&#039;): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$haystack` | **string** |  |
| `$needle` | **string** |  |
| `$collation` | **string** |  |
| `$matchType` | **string** |  |





***

### ensureUTF8

This method takes an input string, checks if it's not valid UTF-8 and
attempts to convert it to UTF-8 if it's not.

```php
public static ensureUTF8(string $input): string
```

Note that currently this can only convert ISO-8859-1 to UTF-8 (latin-1),
anything else will likely fail.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** |  |





***


***
> Automatically generated on 2025-03-18
