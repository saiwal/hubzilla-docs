***

# Permcat





* Full name: `\Zotlabs\Lib\Permcat`



## Properties


### permcats



```php
private array $permcats
```






***

## Methods


### __construct



```php
public __construct(int $channel_id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **int** |  |





***

### listing



```php
public listing(): array
```












***

### fetch



```php
public fetch(string $name): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |


**Return Value:**


*  * \e array with permcats
*  * \e bool \b error if $name not found in permcats true




***

### load_permcats



```php
public load_permcats(mixed $uid): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **mixed** |  |





***

### find_permcat



```php
public static find_permcat(mixed $arr, mixed $name): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |
| `$name` | **mixed** |  |





***

### update



```php
public static update(mixed $channel_id, mixed $name, mixed $permarr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **mixed** |  |
| `$name` | **mixed** |  |
| `$permarr` | **mixed** |  |





***

### delete



```php
public static delete(mixed $channel_id, mixed $name): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **mixed** |  |
| `$name` | **mixed** |  |





***

### assign



```php
public static assign(array $channel, string $role, array $contacts): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **array** |  |
| `$role` | **string** | the name of the role |
| `$contacts` | **array** | an array of contact hashes |





***


***
> Automatically generated on 2025-03-15
