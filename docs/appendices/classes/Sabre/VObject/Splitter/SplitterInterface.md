
# SplitterInterface

VObject splitter.

The splitter is responsible for reading a large vCard or iCalendar object,
and splitting it into multiple objects.

This is for example for Card and CalDAV, which require every event and vcard
to exist in their own objects, instead of one large one.

* Full name: `\Sabre\VObject\Splitter\SplitterInterface`



## Methods


### __construct

Constructor.

```php
public __construct(resource $input): mixed
```

The splitter should receive an readable file stream as its input.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource** |  |





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
> Automatically generated on 2025-03-18
