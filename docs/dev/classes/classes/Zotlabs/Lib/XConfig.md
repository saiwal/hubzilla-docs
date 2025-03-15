
# XConfig





* Full name: `\Zotlabs\Lib\XConfig`




## Methods


### Load



```php
public static Load(string $xchan): void|false
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xchan` | **string** | <br />The observer&#039;s hash |


**Return Value:**

Returns false if xchan is not set




***

### Get



```php
public static Get(string $xchan, string $family, string $key, bool $default = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xchan` | **string** | <br />The observer&#039;s hash |
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to query |
| `$default` | **bool** | (optional) default false |


**Return Value:**

Stored $value or false if it does not exist




***

### Set



```php
public static Set(string $xchan, string $family, string $key, string $value): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xchan` | **string** | <br />The observer&#039;s hash |
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to set |
| `$value` | **string** | <br />The value to store |


**Return Value:**

Stored $value or false




***

### Delete



```php
public static Delete(string $xchan, string $family, string $key): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xchan` | **string** | <br />The observer&#039;s hash |
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to delete |





***


***
> Automatically generated on 2025-03-15
