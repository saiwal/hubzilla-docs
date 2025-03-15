
# Base

Base for cache objects

Classes to be used with {@see \SimplePie\Cache::register()} are expected
to implement this interface.

* Full name: `\SimplePie\Cache\Base`
* **Warning:** this interface is **deprecated**. This means that this interface will likely be removed in a future version.


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TYPE_FEED`|public|string|&#039;spc&#039;|
|`TYPE_IMAGE`|public|string|&#039;spi&#039;|

## Methods


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
