***

# ScheduleCalendarTransp

schedule-calendar-transp property.

This property is a representation of the schedule-calendar-transp property.
This property is defined in:

http://tools.ietf.org/html/rfc6638#section-9.1

Its values are either 'transparent' or 'opaque'. If it's transparent, it
means that this calendar will not be taken into consideration when a
different user queries for free-busy information. If it's 'opaque', it will.

* Full name: `\Sabre\CalDAV\Xml\Property\ScheduleCalendarTransp`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TRANSPARENT`|public| |&#039;transparent&#039;|
|`OPAQUE`|public| |&#039;opaque&#039;|

## Properties


### value

value.

```php
protected string $value
```






***

## Methods


### __construct

Creates the property.

```php
public __construct(string $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





***

### getValue

Returns the current value.

```php
public getValue(): string
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
> Automatically generated on 2025-03-15
