***

# HTMLPurifier_StringHash

This is in almost every respect equivalent to an array except
that it keeps track of which keys were accessed.



* Full name: `\HTMLPurifier_StringHash`
* Parent class: [`ArrayObject`](./ArrayObject.md)



## Properties


### accessed



```php
protected $accessed
```






***

## Methods


### offsetGet

Retrieves a value, and logs the access.

```php
public offsetGet(mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### getAccessed

Returns a lookup array of all array indexes that have been accessed.

```php
public getAccessed(): array
```









**Return Value:**

in form array($index => true).




***

### resetAccessed

Resets the access array.

```php
public resetAccessed(): mixed
```












***


***
> Automatically generated on 2025-03-15
