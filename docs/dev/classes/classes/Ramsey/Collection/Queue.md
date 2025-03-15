***

# Queue

This class provides a basic implementation of `QueueInterface`, to minimize
the effort required to implement this interface.



* Full name: `\Ramsey\Collection\Queue`
* Parent class: [`\Ramsey\Collection\AbstractArray`](./AbstractArray.md)
* This class implements:
[`\Ramsey\Collection\QueueInterface`](./QueueInterface.md)



## Properties


### queueType

The type of elements stored in this queue.

```php
private string $queueType
```

A queue's type is immutable once it is set. For this reason, this
property is set private.




***

### index

The index of the head of the queue.

```php
protected int $index
```






***

## Methods


### __construct

Constructs a queue object of the specified type, optionally with the
specified data.

```php
public __construct(string $queueType, array&lt;array-key,\Ramsey\Collection\T&gt; $data = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$queueType` | **string** | The type (FQCN) associated with this queue. |
| `$data` | **array<array-key,\Ramsey\Collection\T>** | The initial items to store in the collection. |





***

### offsetSet

Sets the given value to the given offset in the array.

```php
public offsetSet(mixed $offset, mixed $value): void
```

Since arbitrary offsets may not be manipulated in a queue, this method
serves only to fulfill the `ArrayAccess` interface requirements. It is
invoked by other operations when adding values to the queue.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** | The offset to set. If `null`, the value may be<br />set at a numerically-indexed offset. |
| `$value` | **mixed** | The value to set at the given offset. |





***

### add

Ensures that this queue contains the specified element (optional
operation).

```php
public add(mixed $element): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** | The element to add to this queue. |


**Return Value:**

`true` if this queue changed as a result of the call.




***

### element

Retrieves, but does not remove, the head of this queue.

```php
public element(): \Ramsey\Collection\T
```









**Return Value:**

the head of this queue.




***

### offer

Inserts the specified element into this queue if it is possible to do so
immediately without violating capacity restrictions.

```php
public offer(mixed $element): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** | The element to add to this queue. |


**Return Value:**

`true` if the element was added to this queue, else `false`.




***

### peek

Retrieves, but does not remove, the head of this queue, or returns `null`
if this queue is empty.

```php
public peek(): \Ramsey\Collection\T|null
```









**Return Value:**

the head of this queue, or `null` if this queue is empty.




***

### poll

Retrieves and removes the head of this queue, or returns `null`
if this queue is empty.

```php
public poll(): \Ramsey\Collection\T|null
```









**Return Value:**

the head of this queue, or `null` if this queue is empty.




***

### remove

Retrieves and removes the head of this queue.

```php
public remove(): \Ramsey\Collection\T
```









**Return Value:**

the head of this queue.




***

### getType

Returns the type associated with this queue.

```php
public getType(): string
```












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
public offsetSet((array-key)|null $offset, \Ramsey\Collection\T $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **(array-key)&#124;null** | The offset to set. If `null`, the value may be<br />set at a numerically-indexed offset. |
| `$value` | **\Ramsey\Collection\T** | The value to set at the given offset. |





**See Also:**

* http://php.net/manual/en/arrayaccess.offsetset.php - ArrayAccess::offsetSet()

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
public unserialize(string $serialized): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$serialized` | **string** | A PHP serialized string to unserialize. |





**See Also:**

* http://php.net/manual/en/serializable.unserialize.php - Serializable::unserialize()

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


***
> Automatically generated on 2025-03-15
