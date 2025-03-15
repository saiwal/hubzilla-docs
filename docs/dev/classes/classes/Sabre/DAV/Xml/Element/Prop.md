***

# Prop

This class is responsible for decoding the {DAV:}prop element as it appears
in {DAV:}property-update.

This class doesn't return an instance of itself. It just returns a
key->value array.

* Full name: `\Sabre\DAV\Xml\Element\Prop`
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

### parseCurrentElement

This function behaves similar to Sabre\Xml\Reader::parseCurrentElement,
but instead of creating deep xml array structures, it will turn any
top-level element it doesn't recognize into either a string, or an
XmlFragment class.

```php
private static parseCurrentElement(\Sabre\Xml\Reader $reader): array
```

This method returns arn array with 2 properties:
* name - A clark-notation XML element name.
* value - The parsed value.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reader` | **\Sabre\Xml\Reader** |  |





***


***
> Automatically generated on 2025-03-15
