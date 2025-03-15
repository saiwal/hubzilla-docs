
# ActiveContextCache

An ActiveContextCache caches active contexts so they can be reused without
the overhead of recomputing them.



* Full name: `\ActiveContextCache`



## Properties


### order

Constructs a new ActiveContextCache.

```php
private $order
```






***

### cache



```php
private $cache
```






***

### size



```php
private $size
```






***

## Methods


### __construct



```php
public __construct(mixed $size = 100): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$size` | **mixed** |  |





***

### get

Gets an active context from the cache based on the current active
context and the new local context.

```php
public get(\stdClass $active_ctx, \stdClass $local_ctx): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the current active context. |
| `$local_ctx` | **\stdClass** | the new local context. |


**Return Value:**

a shared copy of the cached active context or null.




***

### set

Sets an active context in the cache based on the previous active
context and the just-processed local context.

```php
public set(\stdClass $active_ctx, \stdClass $local_ctx, \stdClass $result): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the previous active context. |
| `$local_ctx` | **\stdClass** | the just-processed local context. |
| `$result` | **\stdClass** | the resulting active context. |





***


***
> Automatically generated on 2025-03-15
