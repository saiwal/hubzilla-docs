***

# OAuth1Request





* Full name: `\OAuth1Request`



## Properties


### parameters



```php
private $parameters
```






***

### http_method



```php
private $http_method
```






***

### http_url



```php
private $http_url
```






***

### base_string



```php
public $base_string
```






***

### version



```php
public static $version
```



* This property is **static**.


***

### POST_INPUT



```php
public static $POST_INPUT
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(mixed $http_method, mixed $http_url, mixed $parameters = NULL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$http_method` | **mixed** |  |
| `$http_url` | **mixed** |  |
| `$parameters` | **mixed** |  |





***

### from_request

attempt to build up a request from what was passed to the server

```php
public static from_request(mixed $http_method = NULL, mixed $http_url = NULL, mixed $parameters = NULL): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$http_method` | **mixed** |  |
| `$http_url` | **mixed** |  |
| `$parameters` | **mixed** |  |





***

### from_consumer_and_token

pretty much a helper function to set up the request

```php
public static from_consumer_and_token(mixed $consumer, mixed $token, mixed $http_method, mixed $http_url, mixed $parameters = NULL): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |
| `$http_method` | **mixed** |  |
| `$http_url` | **mixed** |  |
| `$parameters` | **mixed** |  |





***

### set_parameter



```php
public set_parameter(mixed $name, mixed $value, mixed $allow_duplicates = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$value` | **mixed** |  |
| `$allow_duplicates` | **mixed** |  |





***

### get_parameter



```php
public get_parameter(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### get_parameters



```php
public get_parameters(): mixed
```












***

### unset_parameter



```php
public unset_parameter(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### get_signable_parameters

The request parameters, sorted and concatenated into a normalized string.

```php
public get_signable_parameters(): string
```












***

### get_signature_base_string

Returns the base string of this request

```php
public get_signature_base_string(): mixed
```

The base string defined as the method, the url
and the parameters (normalized), each urlencoded
and the concated with &.










***

### get_normalized_http_method

just uppercases the http method

```php
public get_normalized_http_method(): mixed
```












***

### get_normalized_http_url

parses the url and rebuilds it to be
scheme://host/path

```php
public get_normalized_http_url(): mixed
```












***

### to_url

builds a url usable for a GET request

```php
public to_url(): mixed
```












***

### to_postdata

builds the data one would send in a POST request

```php
public to_postdata(): mixed
```












***

### to_header

builds the Authorization: header

```php
public to_header(mixed $realm = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **mixed** |  |





***

### __toString



```php
public __toString(): mixed
```












***

### sign_request



```php
public sign_request(mixed $signature_method, mixed $consumer, mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$signature_method` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |





***

### build_signature



```php
public build_signature(mixed $signature_method, mixed $consumer, mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$signature_method` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |





***

### generate_timestamp

util function: current timestamp

```php
private static generate_timestamp(): mixed
```



* This method is **static**.








***

### generate_nonce

util function: current nonce

```php
private static generate_nonce(): mixed
```



* This method is **static**.








***


***
> Automatically generated on 2025-03-15
