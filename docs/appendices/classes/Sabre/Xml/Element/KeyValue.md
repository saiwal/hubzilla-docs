
# KeyValue

'KeyValue' parses out all child elements from a single node, and outputs a
key=>value struct.

Attributes will be removed, and duplicate child elements are discarded.
Complex values within the elements will be parsed by the 'standard' parser.

For example, KeyValue will parse:

<?xml version="1.0"?>
<s:root xmlns:s="http://sabredav.org/ns">
  <s:elem1>value1</s:elem1>
  <s:elem2>value2</s:elem2>
  <s:elem3 />
</s:root>

Into:

[
  "{http://sabredav.org/ns}elem1" => "value1",
  "{http://sabredav.org/ns}elem2" => "value2",
  "{http://sabredav.org/ns}elem3" => null,
];

* Full name: `\Sabre\Xml\Element\KeyValue`
* This class implements:
[`\Sabre\Xml\Element`](../Element.md)



## Properties


### value

Value to serialize.

```php
protected array $value
```






***

## Methods


### __construct

Constructor.

```php
public __construct(array $value = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





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

Important note 2: You are responsible for advancing the reader to the
next element. Not doing anything will result in a never-ending loop.

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
