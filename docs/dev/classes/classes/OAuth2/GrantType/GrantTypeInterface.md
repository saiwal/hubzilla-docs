***

# GrantTypeInterface

Interface for all OAuth2 Grant Types



* Full name: `\OAuth2\GrantType\GrantTypeInterface`



## Methods


### getQueryStringIdentifier

Get query string identifier

```php
public getQueryStringIdentifier(): string
```












***

### validateRequest



```php
public validateRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***

### getClientId

Get client id

```php
public getClientId(): mixed
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
public getScope(): string|null
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
> Automatically generated on 2025-03-15
