***

# Response

WebDAV {DAV:}response parser.

This class parses the {DAV:}response element, as defined in:

https://tools.ietf.org/html/rfc4918#section-14.24

* Full name: `\Sabre\DAV\Xml\Element\Response`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md)



## Properties


### href

Url for the response.

```php
protected string $href
```






***

### responseProperties

Propertylist, ordered by HTTP status code.

```php
protected array $responseProperties
```






***

### httpStatus

The HTTP status for an entire response.

```php
protected string|null $httpStatus
```

This is currently only used in WebDAV-Sync




***

## Methods


### __construct

The href argument is a url relative to the root of the server. This
class will calculate the full path.

```php
public __construct(string $href, array $responseProperties, string $httpStatus = null): mixed
```

The responseProperties argument is a list of properties
within an array with keys representing HTTP status codes

Besides specific properties, the entire {DAV:}response element may also
have a http status code.
In most cases you don't need it.

This is currently used by the Sync extension to indicate that a node is
deleted.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$href` | **string** |  |
| `$responseProperties` | **array** |  |
| `$httpStatus` | **string** |  |





***

### getHref

Returns the url.

```php
public getHref(): string
```












***

### getHttpStatus

Returns the httpStatus value.

```php
public getHttpStatus(): string
```












***

### getResponseProperties

Returns the property list.

```php
public getResponseProperties(): array
```












***

### xmlSerialize

The serialize method is called during xml writing.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): mixed
```

It should use the $writer argument to encode this object into XML.

Important note: it is not needed to create the parent element. The
parent element is already created, and we only have to worry about
attributes, child elements and text (if any).

Important note 2: If you are writing any new elements, you are also
responsible for closing them.






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
