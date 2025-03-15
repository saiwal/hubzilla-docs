
# Manifest

EPUB manifest structure



* Full name: `\SebLucas\EPubMeta\Data\Manifest`
* This class implements:
[`\Iterator`](../../../Iterator.md), [`\Countable`](../../../Countable.md), [`\ArrayAccess`](../../../ArrayAccess.md)



## Properties


### items



```php
protected array|\SebLucas\EPubMeta\Data\Item[] $items
```






***

## Methods


### createItem

Create and add an Item with the given properties.

```php
public createItem(string $id, string $href, callable $callable, int $size, string|null $mediaType = null): \SebLucas\EPubMeta\Data\Item
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | The identifier of the new item. |
| `$href` | **string** | The relative path of the referenced file in the EPUB. |
| `$callable` | **callable** | A callable to get data from the referenced file in the EPUB. |
| `$size` | **int** | The size of the referenced file in the EPUB. |
| `$mediaType` | **string&#124;null** |  |


**Return Value:**

The newly created Item.



**Throws:**
<p>If $id is already taken.</p>

- [`Exception`](../../../Exception.md)



***

### current

Return the current Item while iterating this Manifest.

```php
public current(): \SebLucas\EPubMeta\Data\Item
```












**See Also:**

* http://php.net/manual/en/iterator.current.php - 

***

### next

Move forward to next Item while iterating this Manifest.

```php
public next(): void
```









**Return Value:**

Any returned value is ignored.




**See Also:**

* http://php.net/manual/en/iterator.next.php - 

***

### key

Return the ID of the current Item while iterating this Manifest.

```php
public key(): string|null
```









**Return Value:**

on success, or null on failure.




**See Also:**

* http://php.net/manual/en/iterator.key.php - 

***

### valid

Checks if current Iterator position is valid.

```php
public valid(): bool
```









**Return Value:**

true on success or false on failure.




**See Also:**

* http://php.net/manual/en/iterator.valid.php - 

***

### rewind

Rewind the Iterator to the first element.

```php
public rewind(): void
```









**Return Value:**

Any returned value is ignored.




**See Also:**

* http://php.net/manual/en/iterator.rewind.php - 

***

### first

Get the first Item of this Manifest.

```php
public first(): \SebLucas\EPubMeta\Data\Item
```












***

### last

Get the last Item of this Manifest.

```php
public last(): \SebLucas\EPubMeta\Data\Item
```












***

### count

Count items of this Manifest.

```php
public count(): int
```









**Return Value:**

The number of Items contained in this Manifest.




**See Also:**

* https://php.net/manual/en/countable.count.php - 

***

### offsetExists

Whether a offset exists

```php
public offsetExists(string $offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **string** | An offset to check for. |


**Return Value:**

true on success or false on failure.




**See Also:**

* https://php.net/manual/en/arrayaccess.offsetexists.php - 

***

### offsetGet

Offset to retrieve

```php
public offsetGet(string $offset): \SebLucas\EPubMeta\Data\Item
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **string** | The offset to retrieve. |





**See Also:**

* https://php.net/manual/en/arrayaccess.offsetget.php - 

***

### offsetSet

Offset to set

```php
public offsetSet(mixed $offset, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** | The offset to assign the value to. |
| `$value` | **mixed** | The value to set. |




**Throws:**

- [`BadMethodCallException`](../../../BadMethodCallException.md)



**See Also:**

* https://php.net/manual/en/arrayaccess.offsetset.php - 

***

### offsetUnset

Offset to unset

```php
public offsetUnset(mixed $offset): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** | The offset to unset. |




**Throws:**

- [`BadMethodCallException`](../../../BadMethodCallException.md)



**See Also:**

* https://php.net/manual/en/arrayaccess.offsetunset.php - 

***


***
> Automatically generated on 2025-03-15
