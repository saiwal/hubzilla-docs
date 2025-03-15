***

# PrincipalPropertySearchReport

PrincipalSearchPropertySetReport request parser.

This class parses the {DAV:}principal-property-search REPORT, as defined
in:

https://tools.ietf.org/html/rfc3744#section-9.4

* Full name: `\Sabre\DAVACL\Xml\Request\PrincipalPropertySearchReport`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### properties

The requested properties.

```php
public array|null $properties
```






***

### searchProperties

searchProperties.

```php
public array $searchProperties
```






***

### applyToPrincipalCollectionSet

By default the property search will be conducted on the url of the http
request. If this is set to true, it will be applied to the principal
collection set instead.

```php
public bool $applyToPrincipalCollectionSet
```






***

### test

Search for principals matching ANY of the properties (OR) or a ALL of
the properties (AND).

```php
public string $test
```

This property is either "anyof" or "allof".




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
