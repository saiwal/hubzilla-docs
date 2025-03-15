
# EventIterator

This class is used to determine new for a recurring event, when the next
events occur.

This iterator may loop infinitely in the future, therefore it is important
that if you use this class, you set hard limits for the amount of iterations
you want to handle.

Note that currently there is not full support for the entire iCalendar
specification, as it's very complex and contains a lot of permutations
that's not yet used very often in software.

For the focus has been on features as they actually appear in Calendaring
software, but this may well get expanded as needed / on demand

The following RRULE properties are supported
  * UNTIL
  * INTERVAL
  * COUNT
  * FREQ=DAILY
    * BYDAY
    * BYHOUR
    * BYMONTH
  * FREQ=WEEKLY
    * BYDAY
    * BYHOUR
    * WKST
  * FREQ=MONTHLY
    * BYMONTHDAY
    * BYDAY
    * BYSETPOS
  * FREQ=YEARLY
    * BYMONTH
    * BYYEARDAY
    * BYWEEKNO
    * BYMONTHDAY (only if BYMONTH is also set)
    * BYDAY (only if BYMONTH is also set)

Anything beyond this is 'undefined', which means that it may get ignored, or
you may get unexpected results. The effect is that in some applications the
specified recurrence may look incorrect, or is missing.

The recurrence iterator also does not yet support THISANDFUTURE.

* Full name: `\Sabre\VObject\Recur\EventIterator`
* This class implements:
[`\Iterator`](../../../Iterator.md)



## Properties


### timeZone

Reference timeZone for floating dates and times.

```php
protected \DateTimeZone $timeZone
```






***

### allDay

True if we're iterating an all-day event.

```php
protected bool $allDay
```






***

### recurIterator

RRULE parser.

```php
protected \Sabre\VObject\Recur\RRuleIterator $recurIterator
```






***

### eventDuration

The duration, in seconds, of the master event.

```php
protected $eventDuration
```

We use this to calculate the DTEND for subsequent events.




***

### masterEvent

A reference to the main (master) event.

```php
protected \Sabre\VObject\Recur\VEVENT $masterEvent
```






***

### overriddenEvents

List of overridden events.

```php
protected array $overriddenEvents
```






***

### overriddenEventsIndex

Overridden event index.

```php
protected array $overriddenEventsIndex
```

Key is timestamp, value is the list of indexes of the item in the $overriddenEvent
property.




***

### exceptions

A list of recurrence-id's that are either part of EXDATE, or are
overridden.

```php
protected array $exceptions
```






***

### counter

Internal event counter.

```php
protected int $counter
```






***

### startDate

The very start of the iteration process.

```php
protected \DateTimeImmutable $startDate
```






***

### currentDate

Where we are currently in the iteration process.

```php
protected \DateTimeImmutable $currentDate
```






***

### nextDate

The next date from the rrule parser.

```php
protected \DateTimeImmutable $nextDate
```

Sometimes we need to temporary store the next date, because an
overridden event came before.




***

### currentOverriddenEvent

The event that overwrites the current iteration.

```php
protected \Sabre\VObject\Recur\VEVENT $currentOverriddenEvent
```






***

## Methods


### __construct

Creates the iterator.

```php
public __construct(\Sabre\VObject\Component|array $input, string|null $uid = null, \DateTimeZone $timeZone = null): mixed
```

There's three ways to set up the iterator.

1. You can pass a VCALENDAR component and a UID.
2. You can pass an array of VEVENTs (all UIDS should match).
3. You can pass a single VEVENT component.

Only the second method is recommended. The other 1 and 3 will be removed
at some point in the future.

The $uid parameter is only required for the first method.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **\Sabre\VObject\Component&#124;array** |  |
| `$uid` | **string&#124;null** |  |
| `$timeZone` | **\DateTimeZone** | reference timezone for floating dates and<br />times |





***

### current

Returns the date for the current position of the iterator.

```php
public current(): \DateTimeImmutable
```












***

### getDtStart

This method returns the start date for the current iteration of the
event.

```php
public getDtStart(): \DateTimeImmutable
```












***

### getDtEnd

This method returns the end date for the current iteration of the
event.

```php
public getDtEnd(): \DateTimeImmutable
```












***

### getEventObject

Returns a VEVENT for the current iterations of the event.

```php
public getEventObject(): \Sabre\VObject\Component\VEvent
```

This VEVENT will have a recurrence id, and its DTSTART and DTEND
altered.










***

### key

Returns the current position of the iterator.

```php
public key(): int
```

This is for us simply a 0-based index.










***

### valid

This is called after next, to see if the iterator is still at a valid
position, or if it's at the end.

```php
public valid(): bool
```












***

### rewind

Sets the iterator back to the starting point.

```php
public rewind(): void
```












***

### next

Advances the iterator with one step.

```php
public next(): void
```












***

### fastForward

Quickly jump to a date in the future.

```php
public fastForward(\DateTimeInterface $dateTime): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dateTime` | **\DateTimeInterface** |  |





***

### isInfinite

Returns true if this recurring event never ends.

```php
public isInfinite(): bool
```












***


***
> Automatically generated on 2025-03-15
