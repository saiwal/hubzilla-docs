***

# Spine

EPUB spine structure



* Full name: `\SebLucas\EPubMeta\Contents\Spine`
* This class implements:
[`\Iterator`](../../../Iterator.md), [`\Countable`](../../../Countable.md), [`\ArrayAccess`](../../../ArrayAccess.md)



## Properties


### tocItem



```php
protected \SebLucas\EPubMeta\Data\Item $tocItem
```






***

### tocFormat



```php
protected string $tocFormat
```






***

### items



```php
protected array|\SebLucas\EPubMeta\Data\Item[] $items
```






***

## Methods


### __construct

Spine Constructor.

```php
public __construct(\SebLucas\EPubMeta\Data\Item $tocItem, string $tocFormat): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tocItem` | **\SebLucas\EPubMeta\Data\Item** | The TOC Item of this Spine. |
| `$tocFormat` | **string** | The TOC Format of this Spine (Toc or Nav). |





***

### getTocItem

Get the TOC Item of this Spine.

```php
public getTocItem(): \SebLucas\EPubMeta\Data\Item
```












***

### getTocFormat

Get the TOC Format of this Spine.

```php
public getTocFormat(): string
```












***

### appendItem

Append an Item to this Spine.

```php
public appendItem(\SebLucas\EPubMeta\Data\Item $item): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **\SebLucas\EPubMeta\Data\Item** | The Item to append to this Spine. |





***

### current

Return the current Item while iterating this Spine.

```php
public current(): \SebLucas\EPubMeta\Data\Item
```












**See Also:**

* http://php.net/manual/en/iterator.current.php - 

***

### next

Move forward to next Item while iterating this Spine.

```php
public next(): void
```









**Return Value:**

Any returned value is ignored.




**See Also:**

* http://php.net/manual/en/iterator.next.php - 

***

### key

Return the index of the current Item while iterating this Spine.

```php
public key(): int|null
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

Get the first Item of this Spine.

```php
public first(): \SebLucas\EPubMeta\Data\Item
```












***

### last

Get the last Item of this Spine.

```php
public last(): \SebLucas\EPubMeta\Data\Item
```












***

### count

Count items of this Spine.

```php
public count(): int
```









**Return Value:**

The number of Items contained in this Spine.




**See Also:**

* https://php.net/manual/en/countable.count.php - 

***

### offsetExists

Whether a offset exists

```php
public offsetExists(int $offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** | An offset to check for. |


**Return Value:**

true on success or false on failure.




**See Also:**

* https://php.net/manual/en/arrayaccess.offsetexists.php - 

***

### offsetGet

Offset to retrieve

```php
public offsetGet(int $offset): \SebLucas\EPubMeta\Data\Item
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** | The offset to retrieve. |





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
