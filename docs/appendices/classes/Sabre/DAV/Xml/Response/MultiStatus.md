
# MultiStatus

WebDAV MultiStatus parser.

This class parses the {DAV:}multistatus response, as defined in:
https://tools.ietf.org/html/rfc4918#section-14.16

And it also adds the {DAV:}synctoken change from:
http://tools.ietf.org/html/rfc6578#section-6.4

* Full name: `\Sabre\DAV\Xml\Response\MultiStatus`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md)



## Properties


### responses

The responses.

```php
protected \Sabre\DAV\Xml\Element\Response[] $responses
```






***

### syncToken

A sync token (from RFC6578).

```php
protected string $syncToken
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\DAV\Xml\Element\Response[] $responses, string $syncToken = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$responses` | **\Sabre\DAV\Xml\Element\Response[]** |  |
| `$syncToken` | **string** |  |





***

### getResponses

Returns the response list.

```php
public getResponses(): \Sabre\DAV\Xml\Element\Response[]
```












***

### getSyncToken

Returns the sync-token, if available.

```php
public getSyncToken(): string|null
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
> Automatically generated on 2025-03-18
