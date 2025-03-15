
# AbstractArray

This class provides a basic implementation of `ArrayInterface`, to minimize
the effort required to implement this interface.



* Full name: `\Ramsey\Collection\AbstractArray`
* This class implements:
[`\Ramsey\Collection\ArrayInterface`](./ArrayInterface.md)
* This class is an **Abstract class**



## Properties


### data

The items of this array.

```php
protected array&lt;array-key,\Ramsey\Collection\T&gt; $data
```






***

## Methods


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


***
> Automatically generated on 2025-03-15
