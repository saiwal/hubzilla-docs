***

# TwitterOAuth

Twitter OAuth class



* Full name: `\TwitterOAuth`



## Properties


### http_code



```php
public $http_code
```






***

### url



```php
public $url
```






***

### host



```php
public $host
```






***

### timeout



```php
public $timeout
```






***

### connecttimeout



```php
public $connecttimeout
```






***

### ssl_verifypeer



```php
public $ssl_verifypeer
```






***

### format



```php
public $format
```






***

### decode_json



```php
public $decode_json
```






***

### http_info



```php
public $http_info
```






***

### useragent



```php
public $useragent
```






***

## Methods


### accessTokenURL

Set API URLS

```php
public accessTokenURL(): mixed
```












***

### authenticateURL



```php
public authenticateURL(): mixed
```












***

### authorizeURL



```php
public authorizeURL(): mixed
```












***

### requestTokenURL



```php
public requestTokenURL(): mixed
```












***

### lastStatusCode

Debug helpers

```php
public lastStatusCode(): mixed
```












***

### lastAPICall



```php
public lastAPICall(): mixed
```












***

### __construct

construct TwitterOAuth object

```php
public __construct(mixed $consumer_key, mixed $consumer_secret, mixed $oauth_token = NULL, mixed $oauth_token_secret = NULL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer_key` | **mixed** |  |
| `$consumer_secret` | **mixed** |  |
| `$oauth_token` | **mixed** |  |
| `$oauth_token_secret` | **mixed** |  |





***

### getRequestToken

Get a request_token from Twitter

```php
public getRequestToken(mixed $oauth_callback = NULL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oauth_callback` | **mixed** |  |





***

### getAuthorizeURL

Get the authorize URL

```php
public getAuthorizeURL(mixed $token, mixed $sign_in_with_twitter = TRUE): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |
| `$sign_in_with_twitter` | **mixed** |  |





***

### getAccessToken

Exchange request token and secret for an access token and
secret, to sign API calls.

```php
public getAccessToken(mixed $oauth_verifier = FALSE): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oauth_verifier` | **mixed** |  |





***

### getXAuthToken

One time exchange of username and password for access token and secret.

```php
public getXAuthToken(mixed $username, mixed $password): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **mixed** |  |
| `$password` | **mixed** |  |





***

### get

GET wrapper for oAuthRequest.

```php
public get(mixed $url, mixed $parameters = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$parameters` | **mixed** |  |





***

### post

POST wrapper for oAuthRequest.

```php
public post(mixed $url, mixed $parameters = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$parameters` | **mixed** |  |





***

### delete

DELETE wrapper for oAuthReqeust.

```php
public delete(mixed $url, mixed $parameters = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$parameters` | **mixed** |  |





***

### oAuthRequest

Format and sign an OAuth / API request

```php
public oAuthRequest(mixed $url, mixed $method, mixed $parameters): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$method` | **mixed** |  |
| `$parameters` | **mixed** |  |





***

### http

Make an HTTP request

```php
public http(mixed $url, mixed $method, mixed $postfields = NULL): \API
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$method` | **mixed** |  |
| `$postfields` | **mixed** |  |


**Return Value:**

results




***

### getHeader

Get the header info to store.

```php
public getHeader(mixed $ch, mixed $header): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ch` | **mixed** |  |
| `$header` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
