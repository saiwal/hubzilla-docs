
# RDateIterator

RRuleParser.

This class receives an RRULE string, and allows you to iterate to get a list
of dates in that recurrence.

For instance, passing: FREQ=DAILY;LIMIT=5 will cause the iterator to contain
5 items, one for each day.

* Full name: `\Sabre\VObject\Recur\RDateIterator`
* This class implements:
[`\Iterator`](../../../Iterator.md)



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

### counter

The current item in the list.

```php
protected int $counter
```

You can get this number with the key() method.




***

### dates

Array with the RRULE dates.

```php
protected array $dates
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
iterator.

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

### parseRDate

This method receives a string from an RRULE property, and populates this
class with all the values.

```php
protected parseRDate(mixed $rdate): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rdate` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
