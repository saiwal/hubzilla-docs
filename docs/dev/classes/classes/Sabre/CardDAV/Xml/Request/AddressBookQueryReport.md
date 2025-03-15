
# AddressBookQueryReport

AddressBookQueryReport request parser.

This class parses the {urn:ietf:params:xml:ns:carddav}addressbook-query
REPORT, as defined in:

http://tools.ietf.org/html/rfc6352#section-8.6

* Full name: `\Sabre\CardDAV\Xml\Request\AddressBookQueryReport`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### properties

An array with requested properties.

```php
public array $properties
```






***

### addressDataProperties

An array with requested vcard properties.

```php
public array $addressDataProperties
```






***

### filters

List of property/component filters.

```php
public array $filters
```

This is an array with filters. Every item is a property filter. Every
property filter has the following keys:
  * name - name of the component to filter on
  * test - anyof or allof
  * is-not-defined - Test for non-existence
  * param-filters - A list of parameter filters on the property
  * text-matches - A list of text values the filter needs to match

Each param-filter has the following keys:
  * name - name of the parameter
  * is-not-defined - Test for non-existence
  * text-match - Match the parameter value

Each text-match in property filters, and the single text-match in
param-filters have the following keys:

  * value - value to match
  * match-type - contains, starts-with, ends-with, equals
  * negate-condition - Do the opposite match
  * collation - Usually i;unicode-casemap




***

### limit

The number of results the client wants.

```php
public int|null $limit
```

null means it wasn't specified, which in most cases means 'all results'.




***

### test

Either 'anyof' or 'allof'.

```php
public string $test
```






***

### contentType

The mimetype of the content that should be returend. Usually
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
