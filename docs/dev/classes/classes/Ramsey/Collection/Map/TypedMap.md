***

# TypedMap

A `TypedMap` represents a map of elements where key and value are typed.

Each element is identified by a key with defined type and a value of defined
type. The keys of the map must be unique. The values on the map can be=
repeated but each with its own different key.

The most common case is to use a string type key, but it's not limited to
this type of keys.

This is a direct implementation of `TypedMapInterface`, provided for the sake
of convenience.

Example usage:

```php
$map = new TypedMap('string', Foo::class);
$map['x'] = new Foo();
foreach ($map as $key => $value) {
    // do something with $key, it will be a Foo::class
}

// this will throw an exception since key must be string
$map[10] = new Foo();

// this will throw an exception since value must be a Foo
$map['bar'] = 'bar';

// initialize map with contents
$map = new TypedMap('string', Foo::class, [
    new Foo(), new Foo(), new Foo()
]);
```

It is preferable to subclass `AbstractTypedMap` to create your own typed map
implementation:

```php
class FooTypedMap extends AbstractTypedMap
{
    public function getKeyType()
    {
        return 'int';
    }

    public function getValueType()
    {
         return Foo::class;
    }
}
```

… but you also may use the `TypedMap` class:

```php
class FooTypedMap extends TypedMap
{
    public function __constructor(array $data = [])
    {
        parent::__construct('int', Foo::class, $data);
    }
}
```

* Full name: `\Ramsey\Collection\Map\TypedMap`
* Parent class: [`\Ramsey\Collection\Map\AbstractTypedMap`](./AbstractTypedMap.md)



## Properties


### keyType

The data type of keys stored in this collection.

```php
private string $keyType
```

A map key's type is immutable once it is set. For this reason, this
property is set private.




***

### valueType

The data type of values stored in this collection.

```php
private string $valueType
```

A map value's type is immutable once it is set. For this reason, this
property is set private.




***

## Methods


### __construct

Constructs a map object of the specified key and value types,
optionally with the specified data.

```php
public __construct(string $keyType, string $valueType, array $data = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keyType` | **string** | The data type of the map&#039;s keys. |
| `$valueType` | **string** | The data type of the map&#039;s values. |
| `$data` | **array** | The initial items to add to this array. |





***

### getKeyType

Return the type used on the key.

```php
public getKeyType(): string
```












***

### getValueType

Return the type forced on the values.

```php
public getValueType(): string
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
public offsetSet(\Ramsey\Collection\Map\K|null $offset, \Ramsey\Collection\Map\T $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **\Ramsey\Collection\Map\K&#124;null** |  |
| `$value` | **\Ramsey\Collection\Map\T** |  |





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

### containsKey

Returns `true` if this map contains a mapping for the specified key.

```php
public containsKey(mixed $key): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to check in the map. |





***

### containsValue

Returns `true` if this map maps one or more keys to the specified value.

```php
public containsValue(mixed $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** | The value to check in the map. |





***

### keys

Return an array of the keys contained in this map.

```php
public keys(): list&lt;array-key&gt;
```












***

### get

Returns the value to which the specified key is mapped, `null` if this
map contains no mapping for the key, or (optionally) `$defaultValue` if
this map contains no mapping for the key.

```php
public get(mixed $key, mixed $defaultValue = null): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to return from the map. |
| `$defaultValue` | **mixed** | The default value to use if `$key` is not found. |


**Return Value:**

the value or `null` if the key could not be found.




***

### put

Associates the specified value with the specified key in this map.

```php
public put(mixed $key, mixed $value): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to put or replace in the map. |
| `$value` | **mixed** | The value to store at `$key`. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### putIfAbsent

Associates the specified value with the specified key in this map only if
it is not already set.

```php
public putIfAbsent(mixed $key, mixed $value): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to put in the map. |
| `$value` | **mixed** | The value to store at `$key`. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### remove

Removes the mapping for a key from this map if it is present.

```php
public remove(mixed $key): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to remove from the map. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### removeIf

Removes the entry for the specified key only if it is currently mapped to
the specified value.

```php
public removeIf(mixed $key, mixed $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to remove from the map. |
| `$value` | **mixed** | The value to match. |


**Return Value:**

true if the value was removed.




***

### replace

Replaces the entry for the specified key only if it is currently mapped
to some value.

```php
public replace(mixed $key, mixed $value): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to replace. |
| `$value` | **mixed** | The value to set at `$key`. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### replaceIf

Replaces the entry for the specified key only if currently mapped to the
specified value.

```php
public replaceIf(mixed $key, mixed $oldValue, mixed $newValue): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** | The key to remove from the map. |
| `$oldValue` | **mixed** | The value to match. |
| `$newValue` | **mixed** | The value to use as a replacement. |


**Return Value:**

true if the value was replaced.




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
