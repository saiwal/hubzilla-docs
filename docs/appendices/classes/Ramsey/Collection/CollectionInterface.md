
# CollectionInterface

A collection represents a group of objects, known as its elements.

Some collections allow duplicate elements and others do not. Some are ordered
and others unordered.

* Full name: `\Ramsey\Collection\CollectionInterface`
* Parent interfaces: [`\Ramsey\Collection\ArrayInterface`](./ArrayInterface.md)

## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`SORT_ASC`|public| |&#039;asc&#039;|
|`SORT_DESC`|public| |&#039;desc&#039;|

## Methods


### add

Ensures that this collection contains the specified element (optional
operation).

```php
public add(\Ramsey\Collection\T $element): bool
```

Returns `true` if this collection changed as a result of the call.
(Returns `false` if this collection does not permit duplicates and
already contains the specified element.)

Collections that support this operation may place limitations on what
elements may be added to this collection. In particular, some
collections will refuse to add `null` elements, and others will impose
restrictions on the type of elements that may be added. Collection
classes should clearly specify in their documentation any restrictions
on what elements may be added.

If a collection refuses to add a particular element for any reason other
than that it already contains the element, it must throw an exception
(rather than returning `false`). This preserves the invariant that a
collection always contains the specified element after this call returns.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to add to the collection. |


**Return Value:**

`true` if this collection changed as a result of the call.




***

### contains

Returns `true` if this collection contains the specified element.

```php
public contains(\Ramsey\Collection\T $element, bool $strict = true): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to check whether the collection contains. |
| `$strict` | **bool** | Whether to perform a strict type check on the value. |





***

### getType

Returns the type associated with this collection.

```php
public getType(): string
```












***

### remove

Removes a single instance of the specified element from this collection,
if it is present.

```php
public remove(\Ramsey\Collection\T $element): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to remove from the collection. |


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

This will always leave the original collection untouched and will return
a new one.






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
public diff(\Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt; $other): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\Ramsey\Collection\CollectionInterface<\Ramsey\Collection\T>** | The collection to check for divergent<br />items. |





***

### intersect

Create a new collection with intersecting item between current and given
collection.

```php
public intersect(\Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt; $other): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\Ramsey\Collection\CollectionInterface<\Ramsey\Collection\T>** | The collection to check for<br />intersecting items. |





***

### merge

Merge current items and items of given collections into a new one.

```php
public merge(\Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt; $collections): \Ramsey\Collection\CollectionInterface&lt;\Ramsey\Collection\T&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$collections` | **\Ramsey\Collection\CollectionInterface<\Ramsey\Collection\T>** | The collections to merge. |





***


## Inherited methods


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


***
> Automatically generated on 2025-03-18
