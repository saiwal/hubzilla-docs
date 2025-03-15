***

# PrincipalMatchReport

PrincipalMatchReport request parser.

This class parses the {DAV:}principal-match REPORT, as defined
in:

https://tools.ietf.org/html/rfc3744#section-9.3

* Full name: `\Sabre\DAVACL\Xml\Request\PrincipalMatchReport`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`SELF`|public| |1|
|`PRINCIPAL_PROPERTY`|public| |2|

## Properties


### type

Must be SELF or PRINCIPAL_PROPERTY.

```php
public int $type
```






***

### properties

List of properties that are being requested for matching resources.

```php
public string[] $properties
```






***

### principalProperty

If $type = PRINCIPAL_PROPERTY, which WebDAV property we should compare
to the current principal.

```php
public string $principalProperty
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
