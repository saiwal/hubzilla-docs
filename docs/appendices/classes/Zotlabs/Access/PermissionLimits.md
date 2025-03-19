
# PermissionLimits





* Full name: `\Zotlabs\Access\PermissionLimits`

**See Also:**

* \Zotlabs\Access\Permissions - 




## Methods


### Std_Limits



```php
public static Std_Limits(): array
```



* This method is **static**.








***

### Set



```php
public static Set(int $channel_id, string $perm, int $perm_limit): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **int** |  |
| `$perm` | **string** |  |
| `$perm_limit` | **int** | one of PERMS_* constants |





***

### Get



```php
public static Get(int $channel_id, string $perm = &#039;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **int** |  |
| `$perm` | **string** | (optional) |





***


***
> Automatically generated on 2025-03-19
