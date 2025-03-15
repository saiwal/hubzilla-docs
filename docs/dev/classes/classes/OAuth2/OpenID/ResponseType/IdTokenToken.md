
# IdTokenToken





* Full name: `\OAuth2\OpenID\ResponseType\IdTokenToken`
* This class implements:
[`\OAuth2\OpenID\ResponseType\IdTokenTokenInterface`](./IdTokenTokenInterface.md)



## Properties


### accessToken



```php
protected \OAuth2\ResponseType\AccessTokenInterface $accessToken
```






***

### idToken



```php
protected \OAuth2\OpenID\ResponseType\IdTokenInterface $idToken
```






***

## Methods


### __construct

Constructor

```php
public __construct(\OAuth2\ResponseType\AccessTokenInterface $accessToken, \OAuth2\OpenID\ResponseType\IdTokenInterface $idToken): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$accessToken` | **\OAuth2\ResponseType\AccessTokenInterface** |  |
| `$idToken` | **\OAuth2\OpenID\ResponseType\IdTokenInterface** |  |





***

### getAuthorizeResponse



```php
public getAuthorizeResponse(array $params, mixed $user_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** |  |
| `$user_id` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
