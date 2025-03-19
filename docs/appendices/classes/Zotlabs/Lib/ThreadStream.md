
# ThreadStream

A list of threads



* Full name: `\Zotlabs\Lib\ThreadStream`



## Properties


### threads



```php
private $threads
```






***

### mode



```php
private $mode
```






***

### observer



```php
private $observer
```






***

### writable



```php
private $writable
```






***

### commentable



```php
private $commentable
```






***

### uploadable



```php
private $uploadable
```






***

### profile_owner



```php
private $profile_owner
```






***

### preview



```php
private $preview
```






***

### prepared_item



```php
private $prepared_item
```






***

### reload



```php
public $reload
```






***

### cipher



```php
private $cipher
```






***

## Methods


### __construct



```php
public __construct(mixed $mode, mixed $preview, mixed $uploadable, mixed $prepared_item = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **mixed** |  |
| `$preview` | **mixed** |  |
| `$uploadable` | **mixed** |  |
| `$prepared_item` | **mixed** |  |





***

### set_mode

Set the mode we'll be displayed on

```php
private set_mode(mixed $mode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **mixed** |  |





***

### get_mode

Get mode

```php
public get_mode(): mixed
```












***

### is_writable

Check if page is writable

```php
public is_writable(): mixed
```












***

### is_commentable



```php
public is_commentable(): mixed
```












***

### is_uploadable



```php
public is_uploadable(): mixed
```












***

### is_preview

Check if page is a preview

```php
public is_preview(): mixed
```












***

### get_profile_owner

Get profile owner

```php
public get_profile_owner(): mixed
```












***

### set_profile_owner



```php
public set_profile_owner(mixed $uid): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uid` | **mixed** |  |





***

### get_observer



```php
public get_observer(): mixed
```












***

### get_cipher



```php
public get_cipher(): mixed
```












***

### add_thread

Add a thread to the conversation

```php
public add_thread(mixed $item): mixed
```

Returns:
_ The inserted item on success
_ false on failure






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### get_template_data

Get data in a form usable by a conversation template

```php
public get_template_data(mixed $conv_responses, mixed $mid_uuid_map): mixed
```

We should find a way to avoid using those arguments (at least most of them)

Returns:
     _ The data requested on success
     _ false on failure






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$conv_responses` | **mixed** |  |
| `$mid_uuid_map` | **mixed** |  |





***

### get_thread

Get a thread based on its item id

```php
private get_thread(mixed $id): mixed
```

Returns:
_ The found item on success
_ false on failure






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***


***
> Automatically generated on 2025-03-19
