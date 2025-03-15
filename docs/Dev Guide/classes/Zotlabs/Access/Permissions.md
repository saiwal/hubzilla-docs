
# Permissions





* Full name: `\Zotlabs\Access\Permissions`




## Methods


### version



```php
public static version(): \Zotlabs\Access\number
```



* This method is **static**.








***

### Perms



```php
public static Perms(string $filter = &#039;&#039;): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filter` | **string** | (optional) only passed to hook permissions_list |


**Return Value:**

Associative array with permissions and short description.




***

### BlockedAnonPerms



```php
public static BlockedAnonPerms(): array
```



* This method is **static**.





**Return Value:**

Associative array with permissions and short description.




***

### FilledPerms



```php
public static FilledPerms(array $arr): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** |  |





***

### OPerms



```php
public static OPerms(array $arr): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | associative perms array &#039;view_stream&#039; =&gt; 1 |


**Return Value:**

Indexed array with elements that look like
* \e string \b name the perm name (e.g. view_stream)
* \e int \b value the value of the perm (e.g. 1)




***

### FilledAutoperms



```php
public static FilledAutoperms(int $channel_id): bool|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **int** |  |





***

### PermsCompare



```php
public static PermsCompare(array $p1, array $p2): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$p1` | **array** | The perms that have to exist in $p2 |
| `$p2` | **array** | The perms to compare against |


**Return Value:**

true if all perms from $p1 exist also in $p2




***

### connect_perms



```php
public static connect_perms(int $channel_id): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **int** | A channel id |


**Return Value:**

Associative array with
* \e array \b perms Permission array
* \e int \b automatic 0 or 1




***


***
> Automatically generated on 2025-03-15
