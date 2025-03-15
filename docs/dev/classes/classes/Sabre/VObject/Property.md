
# Property

Property.

A property is always in a KEY:VALUE structure, and may optionally contain
parameters.

* Full name: `\Sabre\VObject\Property`
* Parent class: [`\Sabre\VObject\Node`](./Node.md)
* This class is an **Abstract class**



## Properties


### name

Property name.

```php
public string $name
```

This will contain a string such as DTSTART, SUMMARY, FN.




***

### group

Property group.

```php
public string|null $group
```

This is only used in vcards




***

### parameters

List of parameters.

```php
public array $parameters
```






***

### value

Current value.

```php
protected mixed $value
```






***

### delimiter

In case this is a multi-value property. This string will be used as a
delimiter.

```php
public string $delimiter
```






***

### lineIndex

The line number in the original iCalendar / vCard file
  that corresponds with the current node
  if the node was read from a file.

```php
public $lineIndex
```






***

### lineString

The line string from the original iCalendar / vCard file
  that corresponds with the current node
  if the node was read from a file.

```php
public $lineString
```






***

## Methods


### __construct

Creates the generic property.

```php
public __construct(\Sabre\VObject\Component $root, string $name, string|array|null $value = null, array $parameters = [], string $group = null, int $lineIndex = null, string $lineString = null): mixed
```

Parameters must be specified in key=>value syntax.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$root` | **\Sabre\VObject\Component** | The root document |
| `$name` | **string** |  |
| `$value` | **string&#124;array&#124;null** |  |
| `$parameters` | **array** | List of parameters |
| `$group` | **string** | The vcard property group |
| `$lineIndex` | **int** |  |
| `$lineString` | **string** |  |





***

### setValue

Updates the current value.

```php
public setValue(string|array $value): mixed
```

This may be either a single, or multiple strings in an array.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string&#124;array** |  |





***

### getValue

Returns the current value.

```php
public getValue(): string
```

This method will always return a singular value. If this was a
multi-value object, some decision will be made first on how to represent
it as a string.

To get the correct multi-value version, use getParts.










***

### setParts

Sets a multi-valued property.

```php
public setParts(array $parts): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parts` | **array** |  |





***

### getParts

Returns a multi-valued property.

```php
public getParts(): array
```

This method always returns an array, if there was only a single value,
it will still be wrapped in an array.










***

### add

Adds a new parameter.

```php
public add(string $name, string|array|null $value = null): mixed
```

If a parameter with same name already existed, the values will be
combined.
If nameless parameter is added, we try to guess its name.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **string&#124;array&#124;null** |  |





***

### parameters

Returns an iterable list of children.

```php
public parameters(): array
```












***

### getValueType

Returns the type of value.

```php
public getValueType(): string
```

This corresponds to the VALUE= parameter. Every property also has a
'default' valueType.


* This method is **abstract**.







***

### setRawMimeDirValue

Sets a raw value coming from a mimedir (iCalendar/vCard) file.

```php
public setRawMimeDirValue(string $val): mixed
```

This has been 'unfolded', so only 1 line will be passed. Unescaping is
not yet done, but parameters are not included.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$val` | **string** |  |





***

### getRawMimeDirValue

Returns a raw mime-dir representation of the value.

```php
public getRawMimeDirValue(): string
```




* This method is **abstract**.







***

### serialize

Turns the object back into a serialized blob.

```php
public serialize(): string
```












***

### getJsonValue

Returns the value, in the format it should be encoded for JSON.

```php
public getJsonValue(): array
```

This method must always return an array.










***

### setJsonValue

Sets the JSON value, as it would appear in a jCard or jCal object.

```php
public setJsonValue(array $value): mixed
```

The value must always be an array.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### jsonSerialize

This method returns an array, with the representation as it should be
encoded in JSON. This is used to create jCard or jCal documents.

```php
public jsonSerialize(): array
```












***

### setXmlValue

Hydrate data from a XML subtree, as it would appear in a xCard or xCal
object.

```php
public setXmlValue(array $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### xmlSerialize

This method serializes the data into XML. This is used to create xCard or
xCal documents.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** | XML writer |





***

### xmlSerializeValue

This method serializes only the value of a property. This is used to
create xCard or xCal documents.

```php
protected xmlSerializeValue(\Sabre\Xml\Writer $writer): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** | XML writer |





***

### __toString

Called when this object is being cast to a string.

```php
public __toString(): string
```

If the property only had a single value, you will get just that. In the
case the property had multiple values, the contents will be escaped and
combined with ,.










***

### offsetExists

Checks if an array element exists.

```php
public offsetExists(mixed $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### offsetGet

Returns a parameter.

```php
public offsetGet(string $name): \Sabre\VObject\Node
```

If the parameter does not exist, null is returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### offsetSet

Creates a new parameter.

```php
public offsetSet(string $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### offsetUnset

Removes one or more parameters with the specified name.

```php
public offsetUnset(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### __clone

This method is automatically called when the object is cloned.

```php
public __clone(): mixed
```

Specifically, this will ensure all child elements are also cloned.










***

### validate

Validates the node for correctness.

```php
public validate(int $options): array
```

The following options are supported:
  - Node::REPAIR - If something is broken, and automatic repair may
                   be attempted.

An array is returned with warnings.

Every item in the array has the following properties:
   * level - (number between 1 and 3 with severity information)
   * message - (human readable message)
   * node - (reference to the offending node)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **int** |  |





***

### destroy

Call this method on a document if you're done using it.

```php
public destroy(): mixed
```

It's intended to remove all circular references, so PHP can easily clean
it up.










***


## Inherited methods


### serialize

Serializes the node into a mimedir format.

```php
public serialize(): string
```




* This method is **abstract**.







***

### jsonSerialize

This method returns an array, with the representation as it should be
encoded in JSON. This is used to create jCard or jCal documents.

```php
public jsonSerialize(): array
```




* This method is **abstract**.







***

### xmlSerialize

This method serializes the data into XML. This is used to create xCard or
xCal documents.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): void
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** | XML writer |





***

### destroy

Call this method on a document if you're done using it.

```php
public destroy(): mixed
```

It's intended to remove all circular references, so PHP can easily clean
it up.










***

### getIterator

Returns the iterator for this object.

```php
public getIterator(): \Sabre\VObject\ElementList
```












***

### setIterator

Sets the overridden iterator.

```php
public setIterator(\Sabre\VObject\ElementList $iterator): mixed
```

Note that this is not actually part of the iterator interface






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iterator` | **\Sabre\VObject\ElementList** |  |





***

### validate

Validates the node for correctness.

```php
public validate(int $options): array
```

The following options are supported:
  Node::REPAIR - May attempt to automatically repair the problem.

This method returns an array with detected problems.
Every element has the following properties:

 * level - problem level.
 * message - A human-readable string describing the issue.
 * node - A reference to the problematic node.

The level means:
  1 - The issue was repaired (only happens if REPAIR was turned on)
  2 - An inconsequential issue
  3 - A severe issue.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **int** |  |





***

### count

Returns the number of elements.

```php
public count(): int
```












***

### offsetExists

Checks if an item exists through ArrayAccess.

```php
public offsetExists(int $offset): bool
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |





***

### offsetGet

Gets an item through ArrayAccess.

```php
public offsetGet(int $offset): mixed
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |





***

### offsetSet

Sets an item through ArrayAccess.

```php
public offsetSet(int $offset, mixed $value): mixed
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |
| `$value` | **mixed** |  |





***

### offsetUnset

Sets an item through ArrayAccess.

```php
public offsetUnset(int $offset): mixed
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |





***


***
> Automatically generated on 2025-03-15
