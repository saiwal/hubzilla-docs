
# UserCredentials





* Full name: `\OAuth2\GrantType\UserCredentials`
* This class implements:
[`\OAuth2\GrantType\GrantTypeInterface`](./GrantTypeInterface.md)



## Properties


### userInfo



```php
private array $userInfo
```






***

### storage



```php
protected \OAuth2\Storage\UserCredentialsInterface $storage
```






***

## Methods


### __construct



```php
public __construct(\OAuth2\Storage\UserCredentialsInterface $storage): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\UserCredentialsInterface** | - REQUIRED Storage class for retrieving user credentials information |





***

### getQueryStringIdentifier

Get query string identifier

```php
public getQueryStringIdentifier(): string
```












***

### validateRequest



```php
public validateRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool|mixed|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |




**Throws:**

- [`LogicException`](../../LogicException.md)



***

### getClientId

Get client id

```php
public getClientId(): mixed|null
```












***

### getUserId

Get user id

```php
public getUserId(): mixed
```












***

### getScope

Get scope

```php
public getScope(): null|string
```












***

### createAccessToken

Create access token

```php
public createAccessToken(\OAuth2\ResponseType\AccessTokenInterface $accessToken, mixed $client_id, mixed $user_id, string $scope): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$accessToken` | **\OAuth2\ResponseType\AccessTokenInterface** |  |
| `$client_id` | **mixed** | - client identifier related to the access token. |
| `$user_id` | **mixed** | - user id associated with the access token |
| `$scope` | **string** | - scopes to be stored in space-separated string. |





***


***
> Automatically generated on 2025-03-18
