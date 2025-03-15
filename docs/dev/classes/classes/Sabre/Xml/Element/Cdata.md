
# Cdata

CDATA element.

This element allows you to easily inject CDATA.

Note that we strongly recommend avoiding CDATA nodes, unless you definitely
know what you're doing, or you're working with unchangeable systems that
require CDATA.

* Full name: `\Sabre\Xml\Element\Cdata`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../XmlSerializable.md)



## Properties


### value

CDATA element value.

```php
protected string $value
```






***

## Methods


### __construct

Constructor.

```php
public __construct(string $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





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
> Automatically generated on 2025-03-15
