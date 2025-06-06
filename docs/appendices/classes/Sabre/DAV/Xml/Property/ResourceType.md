
# ResourceType

{DAV:}resourcetype property.

This class represents the {DAV:}resourcetype property, as defined in:

https://tools.ietf.org/html/rfc4918#section-15.9

* Full name: `\Sabre\DAV\Xml\Property\ResourceType`
* Parent class: [`\Sabre\Xml\Element\Elements`](../../../Xml/Element/Elements.md)
* This class implements:
[`\Sabre\DAV\Browser\HtmlOutput`](../../Browser/HtmlOutput.md)




## Methods


### __construct

Constructor.

```php
public __construct(array|string|null $resourceTypes = null): mixed
```

You can either pass null (for no resourcetype), a string (for a single
resourcetype) or an array (for multiple).

The resourcetype must be specified in clark-notation






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$resourceTypes` | **array&#124;string&#124;null** |  |





***

### getValue

Returns the values in clark-notation.

```php
public getValue(): array
```

For example array('{DAV:}collection')










***

### is

Checks if the principal contains a certain value.

```php
public is(string $type): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** |  |





***

### add

Adds a resourcetype value to this property.

```php
public add(string $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** |  |





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


## Inherited methods


### __construct

Constructor.

```php
public __construct(array $value = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





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

$reader->parseSubTree() will parse the entire sub-tree, and advance to
the next element.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reader` | **\Sabre\Xml\Reader** |  |





***


***
> Automatically generated on 2025-03-18
