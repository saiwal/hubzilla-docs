***

# ElementList

VObject ElementList.

This class represents a list of elements. Lists are the result of queries,
such as doing $vcalendar->vevent where there's multiple VEVENT objects.

* Full name: `\Sabre\VObject\ElementList`
* Parent class: [`ArrayIterator`](../../ArrayIterator.md)




## Methods


### offsetSet

Sets an item through ArrayAccess.

```php
public offsetSet(int $offset, mixed $value): mixed
```








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
