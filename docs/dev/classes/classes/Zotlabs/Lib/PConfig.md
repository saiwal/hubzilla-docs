
# PConfig





* Full name: `\Zotlabs\Lib\PConfig`




## Methods


### Load



```php
public static Load(string $uid): void|false
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **string** | <br />The channel_id |


**Return Value:**

Nothing or false if $uid is null or false




***

### Get



```php
public static Get(string $uid, string $family, string $key, mixed $default = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **string** | <br />The channel_id |
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to query |
| `$default` | **mixed** | (optional, default false)<br />Default value to return if key does not exist |


**Return Value:**

Stored value or false if it does not exist




***

### Set



```php
public static Set(string $uid, string $family, string $key, string $value, string $updated = NULL): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **string** | <br />The channel_id |
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to set |
| `$value` | **string** | <br />The value to store |
| `$updated` | **string** | (optional)<br />The datetime to store |


**Return Value:**

Stored $value or false




***

### Delete



```php
public static Delete(string $uid, string $family, string $key, string $updated = NULL): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **string** | <br />The channel_id |
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to delete |
| `$updated` | **string** | (optional)<br />The datetime to store |





***


***
> Automatically generated on 2025-03-15
