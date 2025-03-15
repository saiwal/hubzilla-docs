***

# CalDAVClient





* Full name: `\Zotlabs\Storage\CalDAVClient`



## Properties


### username



```php
private $username
```






***

### password



```php
private $password
```






***

### url



```php
private $url
```






***

### filepos



```php
public $filepos
```






***

### request_data



```php
public $request_data
```






***

## Methods


### __construct



```php
public __construct(mixed $user, mixed $pass, mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$user` | **mixed** |  |
| `$pass` | **mixed** |  |
| `$url` | **mixed** |  |





***

### set_data



```php
private set_data(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### curl_read



```php
public curl_read(mixed $ch, mixed $fh, mixed $size): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ch` | **mixed** |  |
| `$fh` | **mixed** |  |
| `$size` | **mixed** |  |





***

### ctag_fetch



```php
public ctag_fetch(): mixed
```












***

### detail_fetch



```php
public detail_fetch(): mixed
```












***


***
> Automatically generated on 2025-03-15
