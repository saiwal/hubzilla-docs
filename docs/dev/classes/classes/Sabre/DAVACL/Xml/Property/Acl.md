
# Acl

This class represents the {DAV:}acl property.

The {DAV:}acl property is a full list of access control entries for a
resource.

{DAV:}acl is used as a WebDAV property, but it is also used within the body
of the ACL request.

See:
http://tools.ietf.org/html/rfc3744#section-5.5

* Full name: `\Sabre\DAVACL\Xml\Property\Acl`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md), [`\Sabre\DAV\Browser\HtmlOutput`](../../../DAV/Browser/HtmlOutput.md)



## Properties


### privileges

List of privileges.

```php
protected array $privileges
```






***

### prefixBaseUrl

Whether or not the server base url is required to be prefixed when
serializing the property.

```php
protected bool $prefixBaseUrl
```






***

## Methods


### __construct

Constructor.

```php
public __construct(array $privileges, bool $prefixBaseUrl = true): mixed
```

This object requires a structure similar to the return value from
Sabre\DAVACL\Plugin::getACL().

Each privilege is a an array with at least a 'privilege' property, and a
'principal' property. A privilege may have a 'protected' property as
well.

The prefixBaseUrl should be set to false, if the supplied principal urls
are already full urls. If this is kept to true, the servers base url
will automatically be prefixed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$privileges` | **array** |  |
| `$prefixBaseUrl` | **bool** |  |





***

### getPrivileges

Returns the list of privileges for this property.

```php
public getPrivileges(): array
```












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

### toHtml

Generate html representation for this value.

```php
public toHtml(\Sabre\DAV\Browser\HtmlOutputHelper $html): string
```

The html output is 100% trusted, and no effort is being made to sanitize
it. It's up to the implementor to sanitize user provided values.

The output must be in UTF-8.

The baseUri parameter is a url to the root of the application, and can
be used to construct local links.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **\Sabre\DAV\Browser\HtmlOutputHelper** |  |





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

### serializeAce

Serializes a single access control entry.

```php
private serializeAce(\Sabre\Xml\Writer $writer, array $ace): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** |  |
| `$ace` | **array** |  |





***


***
> Automatically generated on 2025-03-15
