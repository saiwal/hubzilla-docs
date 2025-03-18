
# MapInterface

An object that maps keys to values.

A map cannot contain duplicate keys; each key can map to at most one value.

* Full name: `\Ramsey\Collection\Map\MapInterface`
* Parent interfaces: [`\Ramsey\Collection\ArrayInterface`](../ArrayInterface.md)


## Methods


### containsKey

Returns `true` if this map contains a mapping for the specified key.

```php
public containsKey(array-key $key): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to check in the map. |





***

### containsValue

Returns `true` if this map maps one or more keys to the specified value.

```php
public containsValue(\Ramsey\Collection\Map\T $value): bool
```

This performs a strict type check on the value.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **\Ramsey\Collection\Map\T** | The value to check in the map. |





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
public get(array-key $key, \Ramsey\Collection\Map\T|null $defaultValue = null): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to return from the map. |
| `$defaultValue` | **\Ramsey\Collection\Map\T&#124;null** | The default value to use if `$key` is not found. |


**Return Value:**

the value or `null` if the key could not be found.




***

### put

Associates the specified value with the specified key in this map.

```php
public put(array-key $key, \Ramsey\Collection\Map\T $value): \Ramsey\Collection\Map\T|null
```

If the map previously contained a mapping for the key, the old value is
replaced by the specified value.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to put or replace in the map. |
| `$value` | **\Ramsey\Collection\Map\T** | The value to store at `$key`. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### putIfAbsent

Associates the specified value with the specified key in this map only if
it is not already set.

```php
public putIfAbsent(array-key $key, \Ramsey\Collection\Map\T $value): \Ramsey\Collection\Map\T|null
```

If there is already a value associated with `$key`, this returns that
value without replacing it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to put in the map. |
| `$value` | **\Ramsey\Collection\Map\T** | The value to store at `$key`. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### remove

Removes the mapping for a key from this map if it is present.

```php
public remove(array-key $key): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to remove from the map. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### removeIf

Removes the entry for the specified key only if it is currently mapped to
the specified value.

```php
public removeIf(array-key $key, \Ramsey\Collection\Map\T $value): bool
```

This performs a strict type check on the value.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to remove from the map. |
| `$value` | **\Ramsey\Collection\Map\T** | The value to match. |


**Return Value:**

true if the value was removed.




***

### replace

Replaces the entry for the specified key only if it is currently mapped
to some value.

```php
public replace(array-key $key, \Ramsey\Collection\Map\T $value): \Ramsey\Collection\Map\T|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to replace. |
| `$value` | **\Ramsey\Collection\Map\T** | The value to set at `$key`. |


**Return Value:**

the previous value associated with key, or `null` if
there was no mapping for `$key`.




***

### replaceIf

Replaces the entry for the specified key only if currently mapped to the
specified value.

```php
public replaceIf(array-key $key, \Ramsey\Collection\Map\T $oldValue, \Ramsey\Collection\Map\T $newValue): bool
```

This performs a strict type check on the value.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **array-key** | The key to remove from the map. |
| `$oldValue` | **\Ramsey\Collection\Map\T** | The value to match. |
| `$newValue` | **\Ramsey\Collection\Map\T** | The value to use as a replacement. |


**Return Value:**

true if the value was replaced.




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
