
# SupportedMethodSet

supported-method-set property.

This property is defined in RFC3253, but since it's
so common in other webdav-related specs, it is part of the core server.

This property is defined here:
http://tools.ietf.org/html/rfc3253#section-3.1.3

* Full name: `\Sabre\DAV\Xml\Property\SupportedMethodSet`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md), [`\Sabre\DAV\Browser\HtmlOutput`](../../Browser/HtmlOutput.md)



## Properties


### methods

List of methods.

```php
protected string[] $methods
```






***

## Methods


### __construct

Creates the property.

```php
public __construct(string[] $methods): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$methods` | **string[]** |  |





***

### getValue

Returns the list of supported http methods.

```php
public getValue(): string[]
```












***

### has

Returns true or false if the property contains a specific method.

```php
public has(string $methodName): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$methodName` | **string** |  |





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


***
> Automatically generated on 2025-03-18
