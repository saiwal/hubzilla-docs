
# CurrentUserPrivilegeSet

CurrentUserPrivilegeSet.

This class represents the current-user-privilege-set property. When
requested, it contain all the privileges a user has on a specific node.

* Full name: `\Sabre\DAVACL\Xml\Property\CurrentUserPrivilegeSet`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md), [`\Sabre\DAV\Browser\HtmlOutput`](../../../DAV/Browser/HtmlOutput.md)



## Properties


### privileges

List of privileges.

```php
private array $privileges
```






***

## Methods


### __construct

Creates the object.

```php
public __construct(array $privileges): mixed
```

Pass the privileges in clark-notation






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$privileges` | **array** |  |





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

### has

Returns true or false, whether the specified principal appears in the
list.

```php
public has(string $privilegeName): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$privilegeName` | **string** |  |





***

### getValue

Returns the list of privileges.

```php
public getValue(): array
```












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
> Automatically generated on 2025-03-15
