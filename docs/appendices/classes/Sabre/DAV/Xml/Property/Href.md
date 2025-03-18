
# Href

Href property.

This class represents any WebDAV property that contains a {DAV:}href
element, and there are many.

It can support either 1 or more hrefs. If while unserializing no valid
{DAV:}href elements were found, this property will unserialize itself as
null.

* Full name: `\Sabre\DAV\Xml\Property\Href`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md), [`\Sabre\DAV\Browser\HtmlOutput`](../../Browser/HtmlOutput.md)



## Properties


### hrefs

List of uris.

```php
protected array $hrefs
```






***

### autoPrefix

Automatically prefix the url with the server base directory.

```php
protected bool $autoPrefix
```

Note: use of this property in code was removed in PR:
https://github.com/sabre-io/dav/pull/801
But the property is left here because old data may still exist
that has this property saved.
See discussion in issue:
https://github.com/sabre-io/Baikal/issues/1154.




***

## Methods


### __construct

Constructor.

```php
public __construct(string|string[] $hrefs): mixed
```

You must either pass a string for a single href, or an array of hrefs.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hrefs` | **string&#124;string[]** |  |





***

### getHref

Returns the first Href.

```php
public getHref(): string|null
```












***

### getHrefs

Returns the hrefs as an array.

```php
public getHrefs(): array
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
