***

# Parameter

VObject Parameter.

This class represents a parameter. A parameter is always tied to a property.
In the case of:
  DTSTART;VALUE=DATE:20101108
VALUE=DATE would be the parameter name and value.

* Full name: `\Sabre\VObject\Parameter`
* Parent class: [`\Sabre\VObject\Node`](./Node.md)



## Properties


### name

Parameter name.

```php
public string $name
```






***

### noName

vCard 2.1 allows parameters to be encoded without a name.

```php
public bool $noName
```

We can deduce the parameter name based on its value.




***

### value

Parameter value.

```php
protected string $value
```






***

## Methods


### __construct

Sets up the object.

```php
public __construct(\Sabre\VObject\Document $root, string $name, string $value = null): mixed
```

It's recommended to use the create:: factory method instead.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$root` | **\Sabre\VObject\Document** |  |
| `$name` | **string** |  |
| `$value` | **string** |  |





***

### guessParameterNameByValue

Try to guess property name by value, can be used for vCard 2.1 nameless parameters.

```php
public static guessParameterNameByValue(string $value): string
```

Figuring out what the name should have been. Note that a ton of
these are rather silly in 2014 and would probably rarely be
used, but we like to be complete.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





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
public getValue(): string|null
```

This method will always return a string, or null. If there were multiple
values, it will automatically concatenate them (separated by comma).










***

### setParts

Sets multiple values for this parameter.

```php
public setParts(array $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### getParts

Returns all values for this parameter.

```php
public getParts(): array
```

If there were no values, an empty array will be returned.










***

### addValue

Adds a value to this parameter.

```php
public addValue(string|array $part): mixed
```

If the argument is specified as an array, all items will be added to the
parameter value list.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$part` | **string&#124;array** |  |





***

### has

Checks if this parameter contains the specified value.

```php
public has(string $value): bool
```

This is a case-insensitive match. It makes sense to call this for for
instance the TYPE parameter, to see if it contains a keyword such as
'WORK' or 'FAX'.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





***

### serialize

Turns the object back into a serialized blob.

```php
public serialize(): string
```












***

### jsonSerialize

This method returns an array, with the representation as it should be
encoded in JSON. This is used to create jCard or jCal documents.

```php
public jsonSerialize(): array
```












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

### __toString

Called when this object is being cast to a string.

```php
public __toString(): string
```












***

### getIterator

Returns the iterator for this object.

```php
public getIterator(): \Sabre\VObject\ElementList
```












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
