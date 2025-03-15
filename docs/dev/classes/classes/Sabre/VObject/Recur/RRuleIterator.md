***

# RRuleIterator

RRuleParser.

This class receives an RRULE string, and allows you to iterate to get a list
of dates in that recurrence.

For instance, passing: FREQ=DAILY;LIMIT=5 will cause the iterator to contain
5 items, one for each day.

* Full name: `\Sabre\VObject\Recur\RRuleIterator`
* This class implements:
[`\Iterator`](../../../Iterator.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`dateUpperLimit`|public| |253402300799|

## Properties


### startDate

The reference start date/time for the rrule.

```php
protected \DateTimeInterface $startDate
```

All calculations are based on this initial date.




***

### currentDate

The date of the current iteration. You can get this by calling
->current().

```php
protected \DateTimeInterface $currentDate
```






***

### hourJump

The number of hours that the next occurrence of an event
jumped forward, usually because summer time started and
the requested time-of-day like 0230 did not exist on that
day. And so the event was scheduled 1 hour later at 0330.

```php
protected $hourJump
```






***

### frequency

Frequency is one of: secondly, minutely, hourly, daily, weekly, monthly,
yearly.

```php
protected string $frequency
```






***

### count

The number of recurrences, or 'null' if infinitely recurring.

```php
protected int $count
```






***

### interval

The interval.

```php
protected int $interval
```

If for example frequency is set to daily, interval = 2 would mean every
2 days.




***

### until

The last instance of this recurrence, inclusively.

```php
protected \DateTimeInterface|null $until
```






***

### bySecond

Which seconds to recur.

```php
protected array $bySecond
```

This is an array of integers (between 0 and 60)




***

### byMinute

Which minutes to recur.

```php
protected array $byMinute
```

This is an array of integers (between 0 and 59)




***

### byHour

Which hours to recur.

```php
protected array $byHour
```

This is an array of integers (between 0 and 23)




***

### counter

The current item in the list.

```php
protected int $counter
```

You can get this number with the key() method.




***

### byDay

Which weekdays to recur.

```php
protected array $byDay
```

This is an array of weekdays

This may also be preceded by a positive or negative integer. If present,
this indicates the nth occurrence of a specific day within the monthly or
yearly rrule. For instance, -2TU indicates the second-last tuesday of
the month, or year.




***

### byMonthDay

Which days of the month to recur.

```php
protected array $byMonthDay
```

This is an array of days of the months (1-31). The value can also be
negative. -5 for instance means the 5th last day of the month.




***

### byYearDay

Which days of the year to recur.

```php
protected array $byYearDay
```

This is an array with days of the year (1 to 366). The values can also
be negative. For instance, -1 will always represent the last day of the
year. (December 31st).




***

### byWeekNo

Which week numbers to recur.

```php
protected array $byWeekNo
```

This is an array of integers from 1 to 53. The values can also be
negative. -1 will always refer to the last week of the year.




***

### byMonth

Which months to recur.

```php
protected array $byMonth
```

This is an array of integers from 1 to 12.




***

### bySetPos

Which items in an existing st to recur.

```php
protected array $bySetPos
```

These numbers work together with an existing by* rule. It specifies
exactly which items of the existing by-rule to filter.

Valid values are 1 to 366 and -1 to -366. As an example, this can be
used to recur the last workday of the month.

This would be done by setting frequency to 'monthly', byDay to
'MO,TU,WE,TH,FR' and bySetPos to -1.




***

### weekStart

When the week starts.

```php
protected string $weekStart
```






***

### dayNames

Mappings between the day number and english day name.

```php
protected array $dayNames
```






***

### dayMap

Simple mapping from iCalendar day names to day numbers.

```php
protected array $dayMap
```






***

## Methods


### __construct

Creates the Iterator.

```php
public __construct(string|array $rrule, \DateTimeInterface $start): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rrule` | **string&#124;array** |  |
| `$start` | **\DateTimeInterface** |  |





***

### current



```php
public current(): mixed
```












***

### key

Returns the current item number.

```php
public key(): int
```












***

### valid

Returns whether the current item is a valid item for the recurrence
iterator. This will return false if we've gone beyond the UNTIL or COUNT
statements.

```php
public valid(): bool
```












***

### rewind

Resets the iterator.

```php
public rewind(): void
```












***

### next

Goes on to the next iteration.

```php
public next(): void
```












***

### isInfinite

Returns true if this recurring event never ends.

```php
public isInfinite(): bool
```












***

### fastForward

This method allows you to quickly go to the next occurrence after the
specified date.

```php
public fastForward(\DateTimeInterface $dt): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dt` | **\DateTimeInterface** |  |





***

### startTime

Gets the original start time of the RRULE.

```php
protected startTime(): string
```

The value is formatted as a string with 24-hour:minute:second










***

### advanceTheDate

Advances currentDate by the interval.

```php
protected advanceTheDate(string $interval): void
```

The time is set from the original startDate.
If the recurrence is on a day when summer time started, then the
time on that day may have jumped forward, for example, from 0230 to 0330.
Using the original time means that the next recurrence will be calculated
based on the original start time and the day/week/month/year interval.
So the start time of the next occurrence can correctly revert to 0230.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interval` | **string** |  |





***

### adjustForTimeJumpsOfHourlyEvent

Does the processing for adjusting the time of multi-hourly events when summer time starts.

```php
protected adjustForTimeJumpsOfHourlyEvent(\DateTimeInterface $previousEventDateTime): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$previousEventDateTime` | **\DateTimeInterface** |  |





***

### nextHourly

Does the processing for advancing the iterator for hourly frequency.

```php
protected nextHourly(): mixed
```












***

### nextDaily

Does the processing for advancing the iterator for daily frequency.

```php
protected nextDaily(): mixed
```












***

### nextWeekly

Does the processing for advancing the iterator for weekly frequency.

```php
protected nextWeekly(): mixed
```












***

### nextMonthly

Does the processing for advancing the iterator for monthly frequency.

```php
protected nextMonthly(): mixed
```












***

### nextYearly

Does the processing for advancing the iterator for yearly frequency.

```php
protected nextYearly(): mixed
```












***

### parseRRule

This method receives a string from an RRULE property, and populates this
class with all the values.

```php
protected parseRRule(string|array $rrule): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rrule` | **string&#124;array** |  |





***

### getMonthlyOccurrences

Returns all the occurrences for a monthly frequency with a 'byDay' or
'byMonthDay' expansion for the current month.

```php
protected getMonthlyOccurrences(): array
```

The returned list is an array of integers with the day of month (1-31).










***

### getHours



```php
protected getHours(): mixed
```












***

### getDays



```php
protected getDays(): mixed
```












***

### getMonths



```php
protected getMonths(): mixed
```












***


***
> Automatically generated on 2025-03-15
