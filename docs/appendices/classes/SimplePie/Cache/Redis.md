
# Redis

Caches data to redis

Registered for URLs with the "redis" protocol

For example, `redis://localhost:6379/?timeout=3600&prefix=sp_&dbIndex=0` will
connect to redis on `localhost` on port 6379. All tables will be
prefixed with `simple_primary-` and data will expire after 3600 seconds

* Full name: `\SimplePie\Cache\Redis`
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.
* This class implements:
[`\SimplePie\Cache\Base`](./Base.md)



## Properties


### cache

Redis instance

```php
protected \Redis $cache
```






***

### options

Options

```php
protected array $options
```






***

### name

Cache name

```php
protected string $name
```






***

## Methods


### __construct

Create a new cache object

```php
public __construct(string $location, string $name, mixed $options = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **string** | Location string (from SimplePie::$cache_location) |
| `$name` | **string** | Unique ID for the cache |
| `$options` | **mixed** |  |





***

### setRedisClient



```php
public setRedisClient(\Redis $cache): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cache` | **\Redis** |  |





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
> Automatically generated on 2025-03-18
