
# MkCol

WebDAV Extended MKCOL request parser.

This class parses the {DAV:}mkol request, as defined in:

https://tools.ietf.org/html/rfc5689#section-5.1

* Full name: `\Sabre\DAV\Xml\Request\MkCol`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### properties

The list of properties that will be set.

```php
protected array $properties
```






***

## Methods


### getProperties

Returns a key=>value array with properties that are supposed to get set
during creation of the new collection.

```php
public getProperties(): array
```












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
