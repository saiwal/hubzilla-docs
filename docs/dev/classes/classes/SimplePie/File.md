
# File

Used for fetching remote files and reading local files

Supports HTTP 1.0 via cURL or fsockopen, with spotty HTTP 1.1 support

This class can be overloaded with {@see \SimplePie\SimplePie::set_file_class()}

* Full name: `\SimplePie\File`



## Properties


### url



```php
public $url
```






***

### useragent



```php
public $useragent
```






***

### success



```php
public $success
```






***

### headers



```php
public $headers
```






***

### body



```php
public $body
```






***

### status_code



```php
public $status_code
```






***

### redirects



```php
public $redirects
```






***

### error



```php
public $error
```






***

### method



```php
public $method
```






***

### permanent_url



```php
public $permanent_url
```






***

## Methods


### __construct



```php
public __construct(mixed $url, mixed $timeout = 10, mixed $redirects = 5, mixed $headers = null, mixed $useragent = null, mixed $force_fsockopen = false, mixed $curl_options = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$timeout` | **mixed** |  |
| `$redirects` | **mixed** |  |
| `$headers` | **mixed** |  |
| `$useragent` | **mixed** |  |
| `$force_fsockopen` | **mixed** |  |
| `$curl_options` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
