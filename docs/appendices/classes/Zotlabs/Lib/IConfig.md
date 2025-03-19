
# IConfig





* Full name: `\Zotlabs\Lib\IConfig`




## Methods


### Load



```php
public static Load(mixed& $item): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### Get



```php
public static Get(mixed& $item, mixed $family, mixed $key, mixed $default = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |
| `$family` | **mixed** |  |
| `$key` | **mixed** |  |
| `$default` | **mixed** |  |





***

### Set

IConfig::Set(&$item, $family, $key, $value, $sharing = false);

```php
public static Set(mixed& $item, mixed $family, mixed $key, mixed $value, mixed $sharing = false): mixed
```

$item - item array or item id. If passed an array the iconfig meta information is
   added to the item structure (which will need to be saved with item_store eventually).
   If passed an id, the DB is updated, but may not be federated and/or cloned.
$family - namespace of meta variable
$key - key of meta variable
$value - value of meta variable
$sharing - boolean (default false); if true the meta information is propagated with the item
  to other sites/channels, mostly useful when $item is an array and has not yet been stored/delivered.
  If the meta information is added after delivery and you wish it to be shared, it may be necessary to
  alter the item edited timestamp and invoke the delivery process on the updated item. The edited
  timestamp needs to be altered in order to trigger an item_store_update() at the receiving end.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |
| `$family` | **mixed** |  |
| `$key` | **mixed** |  |
| `$value` | **mixed** |  |
| `$sharing` | **mixed** |  |





***

### Delete



```php
public static Delete(mixed& $item, mixed $family, mixed $key): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |
| `$family` | **mixed** |  |
| `$key` | **mixed** |  |





***


***
> Automatically generated on 2025-03-19
