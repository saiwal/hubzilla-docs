
# DReport





* Full name: `\Zotlabs\Lib\DReport`



## Properties


### location



```php
private $location
```






***

### sender



```php
private $sender
```






***

### recipient



```php
private $recipient
```






***

### name



```php
private $name
```






***

### message_id



```php
private $message_id
```






***

### message_uuid



```php
private $message_uuid
```






***

### status



```php
private $status
```






***

### date



```php
private $date
```






***

## Methods


### __construct



```php
public __construct(mixed $location, mixed $sender, mixed $recipient, mixed $message_id, mixed $message_uuid = &#039;&#039;, mixed $status = &#039;deliver&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **mixed** |  |
| `$sender` | **mixed** |  |
| `$recipient` | **mixed** |  |
| `$message_id` | **mixed** |  |
| `$message_uuid` | **mixed** |  |
| `$status` | **mixed** |  |





***

### update



```php
public update(mixed $status): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$status` | **mixed** |  |





***

### set_name



```php
public set_name(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### addto_update



```php
public addto_update(mixed $status): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$status` | **mixed** |  |





***

### set



```php
public set(mixed $arr): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |





***

### get



```php
public get(): mixed
```












***

### is_storable



```php
public static is_storable(array $dr): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dr` | **array** |  |





***


***
> Automatically generated on 2025-03-18
