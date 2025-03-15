***

# NodeProviderCollection

A collection of NodeProviderInterface objects



* Full name: `\Ramsey\Uuid\Provider\Node\NodeProviderCollection`
* Parent class: [`\Ramsey\Collection\AbstractCollection`](../../../Collection/AbstractCollection.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.




## Methods


### getType

Returns the type associated with this collection.

```php
public getType(): string
```












***

### unserialize

Re-constructs the object from its serialized form

```php
public unserialize(string $serialized): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$serialized` | **string** | The serialized PHP string to unserialize into<br />a UuidInterface instance |





***


## Inherited methods


### __construct

Constructs a new array object.

```php
public __construct(array&lt;array-key,\Ramsey\Collection\T&gt; $data = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array<array-key,\Ramsey\Collection\T>** | The initial items to add to this array. |





***

### getIterator

Returns an iterator for this array.

```php
public getIterator(): \Traversable&lt;array-key,\Ramsey\Collection\T&gt;
```












**See Also:**

* http://php.net/manual/en/iteratoraggregate.getiterator.php - IteratorAggregate::getIterator()

***

### offsetExists

Returns `true` if the given offset exists in this array.

```php
public offsetExists(array-key $offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **array-key** | The offset to check. |





**See Also:**

* http://php.net/manual/en/arrayaccess.offsetexists.php - ArrayAccess::offsetExists()

***

### offsetGet

Returns the value at the specified offset.

```php
public offsetGet(array-key $offset): \Ramsey\Collection\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **array-key** | The offset for which a value should be returned. |


**Return Value:**

the value stored at the offset, or null if the offset
does not exist.




**See Also:**

* http://php.net/manual/en/arrayaccess.offsetget.php - ArrayAccess::offsetGet()

***

### offsetSet

Sets the given value to the given offset in the array.

```php
public offsetSet(mixed $offset, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** | The offset to set. If `null`, the value may be<br />set at a numerically-indexed offset. |
| `$value` | **mixed** | The value to set at the given offset. |





***

### offsetUnset

Removes the given offset and its value from the array.

```php
public offsetUnset(array-key $offset): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **array-key** | The offset to remove from the array. |





**See Also:**

* http://php.net/manual/en/arrayaccess.offsetunset.php - ArrayAccess::offsetUnset()

***

### serialize

Returns a serialized string representation of this array object.

```php
public serialize(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.




**Return Value:**

a PHP serialized string.




**See Also:**

* http://php.net/manual/en/serializable.serialize.php - Serializable::serialize()

***

### __serialize

Returns data suitable for PHP serialization.

```php
public __serialize(): array&lt;array-key,\Ramsey\Collection\T&gt;
```












**See Also:**

* https://www.php.net/manual/en/language.oop5.magic.php#language.oop5.magic.serialize - * https://www.php.net/serialize - 

***

### unserialize

Converts a serialized string representation into an instance object.

```php
public unserialize(mixed $serialized): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$serialized` | **mixed** | A PHP serialized string to unserialize. |





***

### __unserialize

Adds unserialized data to the object.

```php
public __unserialize(array&lt;array-key,\Ramsey\Collection\T&gt; $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array<array-key,\Ramsey\Collection\T>** |  |





***

### count

Returns the number of items in this array.

```php
public count(): int
```












**See Also:**

* http://php.net/manual/en/countable.count.php - Countable::count()

***

### clear

Removes all items from this array.

```php
public clear(): void
```












***

### toArray

Returns a native PHP array representation of this array object.

```php
public toArray(): array&lt;array-key,\Ramsey\Collection\T&gt;
```












***

### isEmpty

Returns `true` if this array is empty.

```php
public isEmpty(): bool
```












***

### extractValue

Extracts the value of the given property or method from the object.

```php
protected extractValue(mixed $object, string $propertyOrMethod): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$object` | **mixed** | The object to extract the value from. |
| `$propertyOrMethod` | **string** | The property or method for which the<br />value should be extracted. |


**Return Value:**

the value extracted from the specified property or method.



**Throws:**
<p>if the method or property is not defined.</p>

- [`ValueExtractionException`](../../../Collection/Exception/ValueExtractionException.md)



***

### toolValueToString

Returns a string representation of the value.

```php
protected toolValueToString(mixed $value): string
```

- null value: `'NULL'`
- boolean: `'TRUE'`, `'FALSE'`
- array: `'Array'`
- scalar: converted-value
- resource: `'(type resource #number)'`
- object with `__toString()`: result of `__toString()`
- object DateTime: ISO 8601 date
- object: `'(className Object)'`
- anonymous function: same as object






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** | the value to return as a string. |





***

### checkType

Returns `true` if value is of the specified type.

```php
protected checkType(string $type, mixed $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | The type to check the value against. |
| `$value` | **mixed** | The value to check. |





***

### add

Ensures that this collection contains the specified element (optional
operation).

```php
public add(mixed $element): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** | The element to add to the collection. |


**Return Value:**

`true` if this collection changed as a result of the call.




***

### contains

Returns `true` if this collection contains the specified element.

```php
public contains(mixed $element, bool $strict = true): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** | The element to check whether the collection contains. |
| `$strict` | **bool** | Whether to perform a strict type check on the value. |





***

### remove

Removes a single instance of the specified element from this collection,
if it is present.

```php
public remove(mixed $element): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** | The element to remove from the collection. |


**Return Value:**

`true` if an element was removed as a result of this call.




***

### column

Returns the values from the given property or method.

```php
public column(string $propertyOrMethod): list
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyOrMethod` | **string** | The property or method name to filter by. |





***

### first

Returns the first item of the collection.

```php
public first(): \Ramsey\Collection\T
```












***

### last

Returns the last item of the collection.

```php
public last(): \Ramsey\Collection\T
```












***

### sort

Sort the collection by a property or method with the given sort order.

```php
public sort(string $propertyOrMethod, string $order = self::SORT_ASC): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```

This will always leave the original collection untouched and will return
a new one.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyOrMethod` | **string** | The property or method to sort by. |
| `$order` | **string** | The sort order for the resulting collection (one of<br />this interface&#039;s `SORT_*` constants). |





***

### filter

Filter out items of the collection which don't match the criteria of
given callback.

```php
public filter(callable $callback): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```

This will always leave the original collection untouched and will return
a new one.

See the {@link http://php.net/manual/en/function.array-filter.php}
for examples of how the `$callback` parameter works.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$callback` | **callable** | A callable to use for filtering elements. |





***

### where

Create a new collection where items match the criteria of given callback.

```php
public where(string $propertyOrMethod, mixed $value): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyOrMethod` | **string** | The property or method to evaluate. |
| `$value` | **mixed** | The value to match. |





***

### map

Apply a given callback method on each item of the collection.

```php
public map(callable $callback): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\TCallbackReturn&gt;
```

This will always leave the original collection untouched. The new
collection is created by mapping the callback to each item of the
original collection.

See the {@link http://php.net/manual/en/function.array-map.php}
for examples of how the `$callback` parameter works.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$callback` | **callable** | A callable to apply to each<br />item of the collection. |





***

### diff

Create a new collection with divergent items between current and given
collection.

```php
public diff(\Ramsey\Collection\CollectionInterface $other): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\Ramsey\Collection\CollectionInterface** | The collection to check for divergent<br />items. |





***

### intersect

Create a new collection with intersecting item between current and given
collection.

```php
public intersect(\Ramsey\Collection\CollectionInterface $other): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\Ramsey\Collection\CollectionInterface** | The collection to check for<br />intersecting items. |





***

### merge

Merge current items and items of given collections into a new one.

```php
public merge(\Ramsey\Collection\CollectionInterface $collections): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$collections` | **\Ramsey\Collection\CollectionInterface** | The collections to merge. |





***

### compareCollectionTypes



```php
private compareCollectionTypes(\Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt; $other): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\Ramsey\Collection\CollectionInterface<\Ramsey\Collection\T>** |  |





***

### getComparator



```php
private getComparator(): \Closure
```












***


***
> Automatically generated on 2025-03-15
