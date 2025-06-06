
# CalendarData

CalendarData parser.

This class parses the {urn:ietf:params:xml:ns:caldav}calendar-data XML
element, as defined in:

https://tools.ietf.org/html/rfc4791#section-9.6

This element is used in three distinct places in the caldav spec, but in
this case, this element class only implements the calendar-data element as
it appears in a DAV:prop element, in a calendar-query or calendar-multiget
REPORT request.

* Full name: `\Sabre\CalDAV\Xml\Filter\CalendarData`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)




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
