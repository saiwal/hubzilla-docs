
# AddressBookMultiGetReport

AddressBookMultiGetReport request parser.

This class parses the {urn:ietf:params:xml:ns:carddav}addressbook-multiget
REPORT, as defined in:

http://tools.ietf.org/html/rfc6352#section-8.7

* Full name: `\Sabre\CardDAV\Xml\Request\AddressBookMultiGetReport`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### properties

An array with requested properties.

```php
public array $properties
```






***

### hrefs

This is an array with the urls that are being requested.

```php
public array $hrefs
```






***

### contentType

The mimetype of the content that should be returned. Usually
text/vcard.

```php
public string $contentType
```






***

### version

The version of vcard data that should be returned. Usually 3.0,
referring to vCard 3.0.

```php
public string $version
```






***

### addressDataProperties

An array with requested vcard properties.

```php
public array $addressDataProperties
```






***

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
> Automatically generated on 2025-03-15
