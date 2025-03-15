***

# Zot6Handler





* Full name: `\Zotlabs\Zot6\Zot6Handler`
* This class implements:
[`\Zotlabs\Zot6\IHandler`](./IHandler.md)




## Methods


### Notify



```php
public Notify(mixed $data, mixed $hub): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$hub` | **mixed** |  |





***

### Rekey



```php
public Rekey(mixed $sender, mixed $data, mixed $hub): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **mixed** |  |
| `$data` | **mixed** |  |
| `$hub` | **mixed** |  |





***

### Refresh



```php
public Refresh(mixed $sender, mixed $recipients, mixed $hub, mixed $force): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **mixed** |  |
| `$recipients` | **mixed** |  |
| `$hub` | **mixed** |  |
| `$force` | **mixed** |  |





***

### Purge



```php
public Purge(mixed $sender, mixed $recipients, mixed $hub): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **mixed** |  |
| `$recipients` | **mixed** |  |
| `$hub` | **mixed** |  |





***

### reply_notify



```php
public static reply_notify(mixed $data, mixed $hub): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$hub` | **mixed** |  |





***

### reply_refresh



```php
public static reply_refresh(array $sender, array $recipients, array $hub, mixed $force): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **array** |  |
| `$recipients` | **array** |  |
| `$hub` | **array** |  |
| `$force` | **mixed** |  |





***

### rekey_request



```php
public static rekey_request(mixed $sender, mixed $data, mixed $hub): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **mixed** |  |
| `$data` | **mixed** |  |
| `$hub` | **mixed** |  |





***

### reply_purge



```php
public static reply_purge(array $sender, array $recipients, array $hub): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **array** |  |
| `$recipients` | **array** |  |
| `$hub` | **array** |  |





***


***
> Automatically generated on 2025-03-15
