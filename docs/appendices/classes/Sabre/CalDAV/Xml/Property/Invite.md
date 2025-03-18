
# Invite

Invite property.

This property encodes the 'invite' property, as defined by
the 'caldav-sharing-02' spec, in the http://calendarserver.org/ns/
namespace.

* Full name: `\Sabre\CalDAV\Xml\Property\Invite`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md)

**See Also:**

* https://trac.calendarserver.org/browser/CalendarServer/trunk/doc/Extensions/caldav-sharing-02.txt - 



## Properties


### sharees

The list of users a calendar has been shared to.

```php
protected \Sabre\DAV\Xml\Element\Sharee[] $sharees
```






***

## Methods


### __construct

Creates the property.

```php
public __construct(\Sabre\DAV\Xml\Element\Sharee[] $sharees): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sharees` | **\Sabre\DAV\Xml\Element\Sharee[]** |  |





***

### getValue

Returns the list of users, as it was passed to the constructor.

```php
public getValue(): array
```












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
