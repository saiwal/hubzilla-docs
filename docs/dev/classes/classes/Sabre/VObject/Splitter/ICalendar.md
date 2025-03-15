***

# ICalendar

Splitter.

This class is responsible for splitting up iCalendar objects.

This class expects a single VCALENDAR object with one or more
calendar-objects inside. Objects with identical UID's will be combined into
a single object.

* Full name: `\Sabre\VObject\Splitter\ICalendar`
* This class implements:
[`\Sabre\VObject\Splitter\SplitterInterface`](./SplitterInterface.md)



## Properties


### vtimezones

Timezones.

```php
protected array $vtimezones
```






***

### objects

iCalendar objects.

```php
protected array $objects
```






***

## Methods


### __construct

Constructor.

```php
public __construct(resource $input, int $options): mixed
```

The splitter should receive an readable file stream as its input.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource** |  |
| `$options` | **int** | parser options, see the OPTIONS constants |





***

### getNext

Every time getNext() is called, a new object will be parsed, until we
hit the end of the stream.

```php
public getNext(): \Sabre\VObject\Component|null
```

When the end is reached, null will be returned.










***


***
> Automatically generated on 2025-03-15
