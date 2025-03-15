***

# Libsync





* Full name: `\Zotlabs\Lib\Libsync`




## Methods


### build_sync_packet



```php
public static build_sync_packet(int $uid, array $packet = null, bool $groups_changed = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **int** | (optional) default 0 |
| `$packet` | **array** | (optional) default null |
| `$groups_changed` | **bool** | (optional) default false |





***

### process_channel_sync_delivery



```php
public static process_channel_sync_delivery(string $sender, array $arr, array $deliveries): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **string** |  |
| `$arr` | **array** |  |
| `$deliveries` | **array** |  |





***

### sync_locations



```php
public static sync_locations(array $sender, array $arr): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **array** |  |
| `$arr` | **array** |  |





***

### keychange



```php
public static keychange(mixed $channel, mixed $arr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$arr` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
