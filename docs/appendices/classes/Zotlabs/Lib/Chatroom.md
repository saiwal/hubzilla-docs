
# Chatroom





* Full name: `\Zotlabs\Lib\Chatroom`




## Methods


### create



```php
public static create(array $channel, array $arr): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **array** |  |
| `$arr` | **array** |  |


**Return Value:**

An associative array containing:
* \e boolean \b success - A boolean success status
* \e string \b message - (optional) A string




***

### destroy



```php
public static destroy(mixed $channel, mixed $arr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$arr` | **mixed** |  |





***

### enter



```php
public static enter(mixed $observer_xchan, mixed $room_id, mixed $status, mixed $client): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$observer_xchan` | **mixed** |  |
| `$room_id` | **mixed** |  |
| `$status` | **mixed** |  |
| `$client` | **mixed** |  |





***

### leave



```php
public static leave(mixed $observer_xchan, mixed $room_id, mixed $client): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$observer_xchan` | **mixed** |  |
| `$room_id` | **mixed** |  |
| `$client` | **mixed** |  |





***

### roomlist



```php
public static roomlist(mixed $uid): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **mixed** |  |





***

### list_count



```php
public static list_count(mixed $uid): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **mixed** |  |





***

### message



```php
public static message(int $uid, int $room_id, string $xchan, string $text): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **int** |  |
| `$room_id` | **int** |  |
| `$xchan` | **string** |  |
| `$text` | **string** |  |





***


***
> Automatically generated on 2025-03-18
