
# Reader

The Reader class expands upon PHP's built-in XMLReader.

The intended usage, is to assign certain XML elements to PHP classes. These
need to be registered using the $elementMap public property.

After this is done, a single call to parse() will parse the entire document,
and delegate sub-sections of the document to element classes.

* Full name: `\Sabre\Xml\Reader`
* Parent class: [`XMLReader`](../../XMLReader.md)




## Methods


### getClark

Returns the current nodename in clark-notation.

```php
public getClark(): string|null
```

For example: "{http://www.w3.org/2005/Atom}feed".
Or if no namespace is defined: "}feed".

This method returns null if we're not currently on an element.










***

### parse

Reads the entire document.

```php
public parse(): array
```

This function returns an array with the following three elements:
   * name - The root element name.
   * value - The value for the root element.
   * attributes - An array of attributes.

This function will also disable the standard libxml error handler (which
usually just results in PHP errors), and throw exceptions instead.










***

### parseGetElements

parseGetElements parses everything in the current sub-tree,
and returns an array of elements.

```php
public parseGetElements(array $elementMap = null): array
```

Each element has a 'name', 'value' and 'attributes' key.

If the element didn't contain sub-elements, an empty array is always
returned. If there was any text inside the element, it will be
discarded.

If the $elementMap argument is specified, the existing elementMap will
be overridden while parsing the tree, and restored after this process.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$elementMap` | **array** |  |





***

### parseInnerTree

Parses all elements below the current element.

```php
public parseInnerTree(array $elementMap = null): array|string|null
```

This method will return a string if this was a text-node, or an array if
there were sub-elements.

If there's both text and sub-elements, the text will be discarded.

If the $elementMap argument is specified, the existing elementMap will
be overridden while parsing the tree, and restored after this process.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$elementMap` | **array** |  |





***

### readText

Reads all text below the current element, and returns this as a string.

```php
public readText(): string
```












***

### parseCurrentElement

Parses the current XML element.

```php
public parseCurrentElement(): array
```

This method returns arn array with 3 properties:
* name - A clark-notation XML element name.
* value - The parsed value.
* attributes - A key-value list of attributes.










***

### parseAttributes

Grabs all the attributes from the current element, and returns them as a
key-value array.

```php
public parseAttributes(): array
```

If the attributes are part of the same namespace, they will simply be
short keys. If they are defined on a different namespace, the attribute
name will be returned in clark-notation.










***

### getDeserializerForElementName

Returns the function that should be used to parse the element identified
by its clark-notation name.

```php
public getDeserializerForElementName(string $name): callable
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





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
