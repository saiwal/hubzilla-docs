
# AllowedSharingModes

AllowedSharingModes.

This property encodes the 'allowed-sharing-modes' property, as defined by
the 'caldav-sharing-02' spec, in the http://calendarserver.org/ns/
namespace.

This property is a representation of the supported-calendar_component-set
property in the CalDAV namespace. It simply requires an array of components,
such as VEVENT, VTODO

* Full name: `\Sabre\CalDAV\Xml\Property\AllowedSharingModes`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md)

**See Also:**

* https://trac.calendarserver.org/browser/CalendarServer/trunk/doc/Extensions/caldav-sharing-02.txt - 



## Properties


### canBeShared

Whether or not a calendar can be shared with another user.

```php
protected bool $canBeShared
```






***

### canBePublished

Whether or not the calendar can be placed on a public url.

```php
protected bool $canBePublished
```






***

## Methods


### __construct

Constructor.

```php
public __construct(bool $canBeShared, bool $canBePublished): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$canBeShared` | **bool** |  |
| `$canBePublished` | **bool** |  |





***

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
> Automatically generated on 2025-03-18
