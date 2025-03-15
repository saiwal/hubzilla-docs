
# Writer

The XML Writer class.

This class works exactly as PHP's built-in XMLWriter, with a few additions.

Namespaces can be registered beforehand, globally. When the first element is
written, namespaces will automatically be declared.

The writeAttribute, startElement and writeElement can now take a
clark-notation element name (example: {http://www.w3.org/2005/Atom}link).

If, when writing the namespace is a known one a prefix will automatically be
selected, otherwise a random prefix will be generated.

Instead of standard string values, the writer can take Element classes (as
defined by this library) to delegate the serialization.

The write() method can take array structures to quickly write out simple xml
trees.

* Full name: `\Sabre\Xml\Writer`
* Parent class: [`XMLWriter`](../../XMLWriter.md)



## Properties


### adhocNamespaces

Any namespace that the writer is asked to write, will be added here.

```php
protected array $adhocNamespaces
```

Any of these elements will get a new namespace definition *every single
time* they are used, but this array allows the writer to make sure that
the prefixes are consistent anyway.




***

### namespacesWritten

When the first element is written, this flag is set to true.

```php
protected bool $namespacesWritten
```

This ensures that the namespaces in the namespaces map are only written
once.




***

## Methods


### write

Writes a value to the output stream.

```php
public write(mixed $value): mixed
```

The following values are supported:
  1. Scalar values will be written as-is, as text.
  2. Null values will be skipped (resulting in a short xml tag).
  3. If a value is an instance of an Element class, writing will be
     delegated to the object.
  4. If a value is an array, two formats are supported.

 Array format 1:
 [
   "{namespace}name1" => "..",
   "{namespace}name2" => "..",
 ]

 One element will be created for each key in this array. The values of
 this array support any format this method supports (this method is
 called recursively).

 Array format 2:

 [
   [
     "name" => "{namespace}name1"
     "value" => "..",
     "attributes" => [
         "attr" => "attribute value",
     ]
   ],
   [
     "name" => "{namespace}name1"
     "value" => "..",
     "attributes" => [
         "attr" => "attribute value",
     ]
   ]
]






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |





***

### startElement

Opens a new element.

```php
public startElement(string $name): bool
```

You can either just use a local elementname, or you can use clark-
notation to start a new element.

Example:

    $writer->startElement('{http://www.w3.org/2005/Atom}entry');

Would result in something like:

    <entry xmlns="http://w3.org/2005/Atom">

Note: this function doesn't have the string typehint, because PHP's
XMLWriter::startElement doesn't either.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### writeElement

Write a full element tag and it's contents.

```php
public writeElement(mixed $name, array|string|object|null $content = null): bool
```

This method automatically closes the element as well.

The element name may be specified in clark-notation.

Examples:

   $writer->writeElement('{http://www.w3.org/2005/Atom}author',null);
   becomes:
   <author xmlns="http://www.w3.org/2005" />

   $writer->writeElement('{http://www.w3.org/2005/Atom}author', [
      '{http://www.w3.org/2005/Atom}name' => 'Evert Pot',
   ]);
   becomes:
   <author xmlns="http://www.w3.org/2005" /><name>Evert Pot</name></author>

Note: this function doesn't have the string typehint, because PHP's
XMLWriter::startElement doesn't either.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$content` | **array&#124;string&#124;object&#124;null** |  |





***

### writeAttributes

Writes a list of attributes.

```php
public writeAttributes(array $attributes): mixed
```

Attributes are specified as a key->value array.

The key is an attribute name. If the key is a 'localName', the current
xml namespace is assumed. If it's a 'clark notation key', this namespace
will be used instead.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attributes` | **array** |  |





***

### writeAttribute

Writes a new attribute.

```php
public writeAttribute(string $name, string $value): bool
```

The name may be specified in clark-notation.

Returns true when successful.

Note: this function doesn't have typehints, because for some reason
PHP's XMLWriter::writeAttribute doesn't either.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **string** |  |





***


## Inherited methods


### pushContext

Create a new "context".

```php
public pushContext(): mixed
```

This allows you to safely modify the elementMap, contextUri or
namespaceMap. After you're done, you can restore the old data again
with popContext.










***

### popContext

Restore the previous "context".

```php
public popContext(): mixed
```












***


***
> Automatically generated on 2025-03-15
