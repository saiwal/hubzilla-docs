***

# SimplePie_Cache_MySQL

Caches data to a MySQL database



* Full name: `\SimplePie_Cache_MySQL`
* Parent class: [`\SimplePie\Cache\MySQL`](./SimplePie/Cache/MySQL.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### prepare_simplepie_object_for_cache

Helper for database conversion

```php
protected static prepare_simplepie_object_for_cache(\SimplePie\SimplePie $data): array
```

Converts a given {@see \SimplePie\Cache\SimplePie} object into data to be stored

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\SimplePie\SimplePie** |  |


**Return Value:**

First item is the serialized data for storage, second item is the unique ID for this item




***

### __construct

Create a new cache object

```php
public __construct(string $location, string $name, \SimplePie\Cache\Base::TYPE_FEED|\SimplePie\Cache\Base::TYPE_IMAGE $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **string** | Location string (from SimplePie::$cache_location) |
| `$name` | **string** | Unique ID for the cache |
| `$type` | **\SimplePie\Cache\Base::TYPE_FEED&#124;\SimplePie\Cache\Base::TYPE_IMAGE** | Either TYPE_FEED for SimplePie data, or TYPE_IMAGE for image data |





***

### save

Save data to the cache

```php
public save(array|\SimplePie\SimplePie $data): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array&#124;\SimplePie\SimplePie** | Data to store in the cache. If passed a SimplePie object, only cache the $data property |


**Return Value:**

Successfulness




***

### load

Retrieve the data saved to the cache

```php
public load(): array
```









**Return Value:**

Data for SimplePie::$data




***

### mtime

Retrieve the last modified time for the cache

```php
public mtime(): int
```









**Return Value:**

Timestamp




***

### touch

Set the last modified time to the current time

```php
public touch(): bool
```









**Return Value:**

Success status




***

### unlink

Remove the cache

```php
public unlink(): bool
```









**Return Value:**

Success status




***


***
> Automatically generated on 2025-03-15
