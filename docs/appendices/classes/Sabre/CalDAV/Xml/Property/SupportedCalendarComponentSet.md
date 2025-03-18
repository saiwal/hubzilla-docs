
# SupportedCalendarComponentSet

SupportedCalendarComponentSet property.

This class represents the
{urn:ietf:params:xml:ns:caldav}supported-calendar-component-set property, as
defined in:

https://tools.ietf.org/html/rfc4791#section-5.2.3

* Full name: `\Sabre\CalDAV\Xml\Property\SupportedCalendarComponentSet`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md)



## Properties


### components

List of supported components.

```php
protected array $components
```

This array will contain values such as VEVENT, VTODO and VJOURNAL.




***

## Methods


### __construct

Creates the property.

```php
public __construct(array $components): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$components` | **array** |  |





***

### getValue

Returns the list of supported components.

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
