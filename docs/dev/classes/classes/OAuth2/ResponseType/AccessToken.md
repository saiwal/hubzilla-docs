
# AccessToken





* Full name: `\OAuth2\ResponseType\AccessToken`
* This class implements:
[`\OAuth2\ResponseType\AccessTokenInterface`](./AccessTokenInterface.md)



## Properties


### tokenStorage



```php
protected \OAuth2\ResponseType\AccessTokenInterface $tokenStorage
```






***

### refreshStorage



```php
protected \OAuth2\Storage\RefreshTokenInterface $refreshStorage
```






***

### config



```php
protected array $config
```






***

## Methods


### __construct



```php
public __construct(\OAuth2\Storage\AccessTokenInterface $tokenStorage, \OAuth2\Storage\RefreshTokenInterface $refreshStorage = null, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokenStorage` | **\OAuth2\Storage\AccessTokenInterface** | - REQUIRED Storage class for saving access token information |
| `$refreshStorage` | **\OAuth2\Storage\RefreshTokenInterface** | - OPTIONAL Storage class for saving refresh token information |
| `$config` | **array** | - OPTIONAL Configuration options for the server |





***

### getAuthorizeResponse

Get authorize response

```php
public getAuthorizeResponse(array $params, mixed $user_id = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** |  |
| `$user_id` | **mixed** |  |





***

### createAccessToken

Handle the creation of access token, also issue refresh token if supported / desirable.

```php
public createAccessToken(mixed $client_id, mixed $user_id, string $scope = null, bool $includeRefreshToken = true): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | - client identifier related to the access token. |
| `$user_id` | **mixed** | - user ID associated with the access token |
| `$scope` | **string** | - OPTIONAL scopes to be stored in space-separated string. |
| `$includeRefreshToken` | **bool** | - if true, a new refresh_token will be added to the response |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-5 - 

***

### generateAccessToken

Generates an unique access token.

```php
protected generateAccessToken(): string
```

Implementing classes may want to override this function to implement
other access token generation schemes.







**Return Value:**

- A unique access token.




***

### generateRefreshToken

Generates an unique refresh token

```php
protected generateRefreshToken(): string
```

Implementing classes may want to override this function to implement
other refresh token generation schemes.







**Return Value:**

- A unique refresh token.




**See Also:**

* \OAuth2\ResponseType\OAuth2::generateAccessToken() - 

***

### revokeToken

Handle the revoking of refresh tokens, and access tokens if supported / desirable
RFC7009 specifies that "If the server is unable to locate the token using
the given hint, it MUST extend its search across all of its supported token types"

```php
public revokeToken(mixed $token, null $tokenTypeHint = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |
| `$tokenTypeHint` | **null** |  |




**Throws:**

- [`RuntimeException`](../../RuntimeException.md)



***


***
> Automatically generated on 2025-03-15
