***

# Hook





* Full name: `\Zotlabs\Extend\Hook`




## Methods


### register



```php
public static register(mixed $hook, mixed $file, mixed $function, mixed $version = 1, mixed $priority): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hook` | **mixed** |  |
| `$file` | **mixed** |  |
| `$function` | **mixed** |  |
| `$version` | **mixed** |  |
| `$priority` | **mixed** |  |





***

### register_array



```php
public static register_array(mixed $file, mixed $arr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |
| `$arr` | **mixed** |  |





***

### unregister



```php
public static unregister(mixed $hook, mixed $file, mixed $function, mixed $version = 1, mixed $priority): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hook` | **mixed** |  |
| `$file` | **mixed** |  |
| `$function` | **mixed** |  |
| `$version` | **mixed** |  |
| `$priority` | **mixed** |  |





***

### unregister_by_file



```php
public static unregister_by_file(string $file): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***

### insert



```php
public static insert(string $hook, string $fn, int $version, int $priority): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hook` | **string** | <br />name of hook to attach callback |
| `$fn` | **string** | <br />function name of callback handler |
| `$version` | **int** | <br />hook interface version, 0 uses two callback params, 1 uses one callback param |
| `$priority` | **int** | <br />currently not implemented in this function, would require the hook array to be resorted |





***


***
> Automatically generated on 2025-03-15
