
# CalendarQueryValidator

CalendarQuery Validator.

This class is responsible for checking if an iCalendar object matches a set
of filters. The main function to do this is 'validate'.

This is used to determine which icalendar objects should be returned for a
calendar-query REPORT request.

* Full name: `\Sabre\CalDAV\CalendarQueryValidator`




## Methods


### validate

Verify if a list of filters applies to the calendar data object.

```php
public validate(\Sabre\VObject\Component\VCalendar $vObject, array $filters): bool
```

The list of filters must be formatted as parsed by \Sabre\CalDAV\CalendarQueryParser






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vObject` | **\Sabre\VObject\Component\VCalendar** |  |
| `$filters` | **array** |  |





***

### validateCompFilters

This method checks the validity of comp-filters.

```php
protected validateCompFilters(\Sabre\VObject\Component $parent, array $filters): bool
```

A list of comp-filters needs to be specified. Also the parent of the
component we're checking should be specified, not the component to check
itself.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parent` | **\Sabre\VObject\Component** |  |
| `$filters` | **array** |  |





***

### validatePropFilters

This method checks the validity of prop-filters.

```php
protected validatePropFilters(\Sabre\VObject\Component $parent, array $filters): bool
```

A list of prop-filters needs to be specified. Also the parent of the
property we're checking should be specified, not the property to check
itself.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parent` | **\Sabre\VObject\Component** |  |
| `$filters` | **array** |  |





***

### validateParamFilters

This method checks the validity of param-filters.

```php
protected validateParamFilters(\Sabre\VObject\Property $parent, array $filters): bool
```

A list of param-filters needs to be specified. Also the parent of the
parameter we're checking should be specified, not the parameter to check
itself.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parent` | **\Sabre\VObject\Property** |  |
| `$filters` | **array** |  |





***

### validateTextMatch

This method checks the validity of a text-match.

```php
protected validateTextMatch(\Sabre\VObject\Node|string $check, array $textMatch): bool
```

A single text-match should be specified as well as the specific property
or parameter we need to validate.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$check` | **\Sabre\VObject\Node&#124;string** | value to check against |
| `$textMatch` | **array** |  |





***

### validateTimeRange

Validates if a component matches the given time range.

```php
protected validateTimeRange(\Sabre\VObject\Node $component, \DateTime $start, \DateTime $end): bool
```

This is all based on the rules specified in rfc4791, which are quite
complex.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$component` | **\Sabre\VObject\Node** |  |
| `$start` | **\DateTime** |  |
| `$end` | **\DateTime** |  |





***


***
> Automatically generated on 2025-03-18
