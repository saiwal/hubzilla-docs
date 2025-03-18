
# Queue





* Full name: `\Zotlabs\Lib\Queue`




## Methods


### update



```php
public static update(mixed $id, mixed $add_priority): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |
| `$add_priority` | **mixed** |  |





***

### remove



```php
public static remove(mixed $id, mixed $channel_id): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |
| `$channel_id` | **mixed** |  |





***

### remove_by_posturl



```php
public static remove_by_posturl(mixed $posturl): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$posturl` | **mixed** |  |





***

### set_delivered



```php
public static set_delivered(mixed $id, mixed $channel): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |
| `$channel` | **mixed** |  |





***

### insert



```php
public static insert(mixed $arr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |





***

### deliver



```php
public static deliver(mixed $outq, mixed $immediate = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$outq` | **mixed** |  |
| `$immediate` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
