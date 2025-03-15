
# BirthdayCalendarGenerator

This class generates birthday calendars.



* Full name: `\Sabre\VObject\BirthdayCalendarGenerator`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DEFAULT_YEAR`|public| |2000|

## Properties


### objects

Input objects.

```php
protected array $objects
```






***

### format

Output format for the SUMMARY.

```php
protected string $format
```






***

## Methods


### __construct

Creates the generator.

```php
public __construct(mixed $objects = null): mixed
```

Check the setTimeRange and setObjects methods for details about the
arguments.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$objects` | **mixed** |  |





***

### setObjects

Sets the input objects.

```php
public setObjects(mixed $objects): mixed
```

You must either supply a vCard as a string or as a Component/VCard object.
It's also possible to supply an array of strings or objects.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$objects` | **mixed** |  |





***

### setFormat

Sets the output format for the SUMMARY.

```php
public setFormat(string $format): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **string** |  |





***

### getResult

Parses the input data and returns a VCALENDAR.

```php
public getResult(): mixed
```












***


***
> Automatically generated on 2025-03-15
