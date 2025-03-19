
# Verify





* Full name: `\Zotlabs\Lib\Verify`




## Methods


### create



```php
public static create(mixed $type, mixed $channel_id, mixed $token, mixed $meta): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **mixed** |  |
| `$channel_id` | **mixed** |  |
| `$token` | **mixed** |  |
| `$meta` | **mixed** |  |





***

### match



```php
public static match(mixed $type, mixed $channel_id, mixed $token, mixed $meta): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **mixed** |  |
| `$channel_id` | **mixed** |  |
| `$token` | **mixed** |  |
| `$meta` | **mixed** |  |





***

### get_meta



```php
public static get_meta(mixed $type, mixed $channel_id, mixed $token): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **mixed** |  |
| `$channel_id` | **mixed** |  |
| `$token` | **mixed** |  |





***

### purge



```php
public static purge(string $type, string $interval): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | Verify type |
| `$interval` | **string** | SQL compatible time interval |





***


***
> Automatically generated on 2025-03-19
