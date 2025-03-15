
# CodeIdToken





* Full name: `\OAuth2\OpenID\ResponseType\CodeIdToken`
* This class implements:
[`\OAuth2\OpenID\ResponseType\CodeIdTokenInterface`](./CodeIdTokenInterface.md)



## Properties


### authCode



```php
protected \OAuth2\OpenID\ResponseType\AuthorizationCodeInterface $authCode
```






***

### idToken



```php
protected \OAuth2\OpenID\ResponseType\IdTokenInterface $idToken
```






***

## Methods


### __construct



```php
public __construct(\OAuth2\OpenID\ResponseType\AuthorizationCodeInterface $authCode, \OAuth2\OpenID\ResponseType\IdTokenInterface $idToken): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$authCode` | **\OAuth2\OpenID\ResponseType\AuthorizationCodeInterface** |  |
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
