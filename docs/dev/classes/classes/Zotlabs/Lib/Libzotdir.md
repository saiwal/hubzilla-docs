
# Libzotdir





* Full name: `\Zotlabs\Lib\Libzotdir`




## Methods


### find_upstream_directory



```php
public static find_upstream_directory(int $dirmode): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dirmode` | **int** |  |





***

### check_upstream_directory

Directories may come and go over time. We will need to check that our
directory server is still valid occasionally, and reset to something that
is if our directory has gone offline for any reason

```php
public static check_upstream_directory(): mixed
```



* This method is **static**.








***

### get_directory_setting



```php
public static get_directory_setting(mixed $observer, mixed $setting): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$observer` | **mixed** |  |
| `$setting` | **mixed** |  |





***

### dir_sort_links



```php
public static dir_sort_links(): mixed
```



* This method is **static**.








***

### sync_directories



```php
public static sync_directories(int $dirmode): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dirmode` | **int** | ; |





***

### update_directory_entry



```php
public static update_directory_entry(array $ud): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ud` | **array** | Entry from update table |





***

### local_dir_update



```php
public static local_dir_update(int $uid, bool $force): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **int** |  |
| `$force` | **bool** |  |





***

### import_directory_profile



```php
public static import_directory_profile(string $hash, array $profile): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** |  |
| `$profile` | **array** |  |


**Return Value:**

$updated if something changed




***

### import_directory_keywords



```php
public static import_directory_keywords(string $hash, array $keywords): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** | An xtag_hash |
| `$keywords` | **array** |  |





***

### update



```php
public static update(string $hash, string $addr, bool $bump_date = true, mixed $flag = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** | the channel hash |
| `$addr` | **string** | the channel url |
| `$bump_date` | **bool** | (optional) default true |
| `$flag` | **mixed** |  |





***

### delete_by_hash



```php
public static delete_by_hash(string $hash): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** | the channel hash |





***


***
> Automatically generated on 2025-03-15
