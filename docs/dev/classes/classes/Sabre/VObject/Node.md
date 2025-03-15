***

# Node

A node is the root class for every element in an iCalendar of vCard object.



* Full name: `\Sabre\VObject\Node`
* This class implements:
[`\IteratorAggregate`](../../IteratorAggregate.md), [`\ArrayAccess`](../../ArrayAccess.md), [`\Countable`](../../Countable.md), [`\JsonSerializable`](../../JsonSerializable.md), [`\Sabre\Xml\XmlSerializable`](../Xml/XmlSerializable.md)
* This class is an **Abstract class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`REPAIR`|public| |1|
|`PROFILE_CARDDAV`|public| |2|
|`PROFILE_CALDAV`|public| |4|

## Properties


### parent

Reference to the parent object, if this is not the top object.

```php
public \Sabre\VObject\Node $parent
```






***

### iterator

Iterator override.

```php
protected \Sabre\VObject\ElementList $iterator
```






***

### root

The root document.

```php
protected \Sabre\VObject\Component $root
```






***

## Methods


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
