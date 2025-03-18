
# Config





* Full name: `\Zotlabs\Lib\Config`




## Methods


### Load



```php
public static Load(string $family, mixed $recursionCounter): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$family` | **string** | <br />The category of the configuration value |
| `$recursionCounter` | **mixed** |  |





***

### Set



```php
public static Set(string $family, string $key, mixed $value): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to set |
| `$value` | **mixed** | <br />The value to store in the configuration |


**Return Value:**


Return the set value, or false if the database update failed




***

### Get



```php
public static Get(string $family, string $key, mixed $default = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to query |
| `$default` | **mixed** | (optional) default false |


**Return Value:**

Return value or false on error or if not set




***

### Delete



```php
public static Delete(string $family, string $key): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to delete |





***

### get_from_storage



```php
private static get_from_storage(string $family, string $key): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$family` | **string** | <br />The category of the configuration value |
| `$key` | **string** | <br />The configuration key to query |





***


***
> Automatically generated on 2025-03-18
