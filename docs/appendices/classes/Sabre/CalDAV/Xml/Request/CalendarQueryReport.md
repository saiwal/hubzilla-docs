
# CalendarQueryReport

CalendarQueryReport request parser.

This class parses the {urn:ietf:params:xml:ns:caldav}calendar-query
REPORT, as defined in:

https://tools.ietf.org/html/rfc4791#section-7.9

* Full name: `\Sabre\CalDAV\Xml\Request\CalendarQueryReport`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### properties

An array with requested properties.

```php
public array $properties
```






***

### filters

List of property/component filters.

```php
public array $filters
```






***

### expand

If the calendar data must be expanded, this will contain an array with 2
elements: start and end.

```php
public array|null $expand
```

Each may be a DateTime or null.




***

### contentType

The mimetype of the content that should be returend. Usually
text/calendar.

```php
public string $contentType
```






***

### version

The version of calendar-data that should be returned. Usually '2.0',
referring to iCalendar 2.0.

```php
public string $version
```






***

## Methods


### xmlDeserialize

The deserialize method is called during xml parsing.

```php
public static xmlDeserialize(\Sabre\Xml\Reader $reader): mixed
```

This method is called statically, this is because in theory this method
may be used as a type of constructor, or factory method.

Often you want to return an instance of the current class, but you are
free to return other data as well.

You are responsible for advancing the reader to the next element. Not
doing anything will result in a never-ending loop.

If you just want to skip parsing for this element altogether, you can
just call $reader->next();

$reader->parseInnerTree() will parse the entire sub-tree, and advance to
the next element.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reader` | **\Sabre\Xml\Reader** |  |





***


***
> Automatically generated on 2025-03-18
