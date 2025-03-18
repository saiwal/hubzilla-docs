
# Service

XML service for WebDAV.



* Full name: `\Sabre\DAV\Xml\Service`
* Parent class: [`\Sabre\Xml\Service`](../../Xml/Service.md)



## Properties


### elementMap

This is a list of XML elements that we automatically map to PHP classes.

```php
public array $elementMap
```

For instance, this list may contain an entry `{DAV:}propfind` that would
be mapped to Sabre\DAV\Xml\Request\PropFind




***

### namespaceMap

This is a default list of namespaces.

```php
public array $namespaceMap
```

If you are defining your own custom namespace, add it here to reduce
bandwidth and improve legibility of xml bodies.




***



## Inherited methods


### getReader

Returns a fresh XML Reader.

```php
public getReader(): \Sabre\Xml\Reader
```












***

### getWriter

Returns a fresh xml writer.

```php
public getWriter(): \Sabre\Xml\Writer
```












***

### parse

Parses a document in full.

```php
public parse(string|resource $input, string $contextUri = null, string& $rootElementName = null): array|object|string
```

Input may be specified as a string or readable stream resource.
The returned value is the value of the root document.

Specifying the $contextUri allows the parser to figure out what the URI
of the document was. This allows relative URIs within the document to be
expanded easily.

The $rootElementName is specified by reference and will be populated
with the root element name of the document.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string&#124;resource** |  |
| `$contextUri` | **string** |  |
| `$rootElementName` | **string** |  |




**Throws:**

- [`ParseException`](../../Xml/ParseException.md)



***

### expect

Parses a document in full, and specify what the expected root element
name is.

```php
public expect(string|string[] $rootElementName, string|resource $input, string $contextUri = null): array|object|string
```

This function works similar to parse, but the difference is that the
user can specify what the expected name of the root element should be,
in clark notation.

This is useful in cases where you expected a specific document to be
passed, and reduces the amount of if statements.

It's also possible to pass an array of expected rootElements if your
code may expect more than one document type.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rootElementName` | **string&#124;string[]** |  |
| `$input` | **string&#124;resource** |  |
| `$contextUri` | **string** |  |




**Throws:**

- [`ParseException`](../../Xml/ParseException.md)



***

### write

Generates an XML document in one go.

```php
public write(string $rootElementName, string|array|object|\Sabre\Xml\XmlSerializable $value, string $contextUri = null): string
```

The $rootElement must be specified in clark notation.
The value must be a string, an array or an object implementing
XmlSerializable. Basically, anything that's supported by the Writer
object.

$contextUri can be used to specify a sort of 'root' of the PHP application,
in case the xml document is used as a http response.

This allows an implementor to easily create URI's relative to the root
of the domain.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rootElementName` | **string** |  |
| `$value` | **string&#124;array&#124;object&#124;\Sabre\Xml\XmlSerializable** |  |
| `$contextUri` | **string** |  |





***

### mapValueObject

Map an XML element to a PHP class.

```php
public mapValueObject(string $elementName, string $className): mixed
```

Calling this function will automatically set up the Reader and Writer
classes to turn a specific XML element to a PHP class.

For example, given a class such as :

class Author {
  public $firstName;
  public $lastName;
}

and an XML element such as:

<author xmlns="http://example.org/ns">
  <firstName>...</firstName>
  <lastName>...</lastName>
</author>

These can easily be mapped by calling:

$service->mapValueObject('{http://example.org}author', 'Author');






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$elementName` | **string** |  |
| `$className` | **string** |  |





***

### writeValueObject

Writes a value object.

```php
public writeValueObject(object $object, string $contextUri = null): mixed
```

This function largely behaves similar to write(), except that it's
intended specifically to serialize a Value Object into an XML document.

The ValueObject must have been previously registered using
mapValueObject().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$object` | **object** |  |
| `$contextUri` | **string** |  |




**Throws:**

- [`InvalidArgumentException`](../../../InvalidArgumentException.md)



***

### parseClarkNotation

Parses a clark-notation string, and returns the namespace and element
name components.

```php
public static parseClarkNotation(string $str): array
```

If the string was invalid, it will throw an InvalidArgumentException.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




**Throws:**

- [`InvalidArgumentException`](../../../InvalidArgumentException.md)



***


***
> Automatically generated on 2025-03-18
