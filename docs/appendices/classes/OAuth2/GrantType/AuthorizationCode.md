
# AuthorizationCode





* Full name: `\OAuth2\GrantType\AuthorizationCode`
* This class implements:
[`\OAuth2\GrantType\GrantTypeInterface`](./GrantTypeInterface.md)



## Properties


### storage



```php
protected \OAuth2\Storage\AuthorizationCodeInterface $storage
```






***

### authCode



```php
protected array $authCode
```






***

## Methods


### __construct



```php
public __construct(\OAuth2\Storage\AuthorizationCodeInterface $storage): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\AuthorizationCodeInterface** | - REQUIRED Storage class for retrieving authorization code information |





***

### getQueryStringIdentifier

Get query string identifier

```php
public getQueryStringIdentifier(): string
```












***

### validateRequest

Validate the OAuth request

```php
public validateRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### getClientId

Get the client id

```php
public getClientId(): mixed
```












***

### getScope

Get the scope

```php
public getScope(): string
```












***

### getUserId

Get the user id

```php
public getUserId(): mixed
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
