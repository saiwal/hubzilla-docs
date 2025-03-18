
# SimplePie_Cache_DB

Base class for database-based caches



* Full name: `\SimplePie_Cache_DB`
* Parent class: [`\SimplePie\Cache\DB`](./SimplePie/Cache/DB.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.
* This class is an **Abstract class**






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


***
> Automatically generated on 2025-03-18
