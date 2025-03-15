***

# SupportedCalendarData

Supported-calendar-data property.

This property is a representation of the supported-calendar-data property
in the CalDAV namespace. SabreDAV only has support for text/calendar;2.0
so the value is currently hardcoded.

This property is defined in:
http://tools.ietf.org/html/rfc4791#section-5.2.4

* Full name: `\Sabre\CalDAV\Xml\Property\SupportedCalendarData`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md)




## Methods


### xmlSerialize

The xmlSerialize method is called during xml writing.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): mixed
```

Use the $writer argument to write its own xml serialization.

An important note: do _not_ create a parent element. Any element
implementing XmlSerializable should only ever write what's considered
its 'inner xml'.

The parent of the current element is responsible for writing a
containing element.

This allows serializers to be re-used for different element names.

If you are opening new elements, you must also close them again.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** |  |





***


***
> Automatically generated on 2025-03-15
