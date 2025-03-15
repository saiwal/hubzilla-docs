***

# LocalHref

LocalHref property.

Like the Href property, this element represents {DAV:}href. The difference
is that this is used strictly for paths on the server. The LocalHref property
will prepare the path so it's a valid URI.

These two objects behave identically:
   new LocalHref($path)
   new Href(\Sabre\HTTP\encodePath($path))

LocalPath basically ensures that your spaces are %20, and everything that
needs to be is uri encoded.

* Full name: `\Sabre\DAV\Xml\Property\LocalHref`
* Parent class: [`\Sabre\DAV\Xml\Property\Href`](./Href.md)




## Methods


### __construct

Constructor.

```php
public __construct(string|string[] $hrefs): mixed
```

You must either pass a string for a single href, or an array of hrefs.

If auto-prefix is set to false, the hrefs will be treated as absolute
and not relative to the servers base uri.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hrefs` | **string&#124;string[]** |  |





***


## Inherited methods


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
> Automatically generated on 2025-03-15
