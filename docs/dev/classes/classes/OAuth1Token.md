
# OAuth1Token





* Full name: `\OAuth1Token`



## Properties


### key



```php
public $key
```






***

### secret



```php
public $secret
```






***

### expires



```php
public $expires
```






***

### scope



```php
public $scope
```






***

### uid



```php
public $uid
```






***

## Methods


### __construct

key = the token
secret = the token secret

```php
public __construct(mixed $key, mixed $secret): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |
| `$secret` | **mixed** |  |





***

### to_string

generates the basic string serialization of a token that a server
would respond to request_token and access_token calls with

```php
public to_string(): mixed
```












***

### __toString



```php
public __toString(): mixed
```












***


***
> Automatically generated on 2025-03-15
