
# JwtAccessToken





* Full name: `\OAuth2\ResponseType\JwtAccessToken`
* Parent class: [`\OAuth2\ResponseType\AccessToken`](./AccessToken.md)



## Properties


### publicKeyStorage



```php
protected $publicKeyStorage
```






***

### encryptionUtil



```php
protected $encryptionUtil
```






***

## Methods


### __construct



```php
public __construct(\OAuth2\Storage\PublicKeyInterface $publicKeyStorage = null, \OAuth2\Storage\AccessTokenInterface $tokenStorage = null, \OAuth2\Storage\RefreshTokenInterface $refreshStorage = null, array $config = array(), \OAuth2\Encryption\EncryptionInterface $encryptionUtil = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$publicKeyStorage` | **\OAuth2\Storage\PublicKeyInterface** | - |
| `$tokenStorage` | **\OAuth2\Storage\AccessTokenInterface** | - |
| `$refreshStorage` | **\OAuth2\Storage\RefreshTokenInterface** | - |
| `$config` | **array** | - array with key store_encrypted_token_string (bool true)<br />whether the entire encrypted string is stored,<br />or just the token ID is stored |
| `$encryptionUtil` | **\OAuth2\Encryption\EncryptionInterface** | - |





***

### createAccessToken

Handle the creation of access token, also issue refresh token if supported / desirable.

```php
public createAccessToken(mixed $client_id, mixed $user_id, string $scope = null, bool $includeRefreshToken = true): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | - Client identifier related to the access token. |
| `$user_id` | **mixed** | - User ID associated with the access token |
| `$scope` | **string** | - (optional) Scopes to be stored in space-separated string. |
| `$includeRefreshToken` | **bool** | - If true, a new refresh_token will be added to the response |


**Return Value:**

- The access token




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-5 - 

***

### encodeToken



```php
protected encodeToken(array $token, mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **array** |  |
| `$client_id` | **mixed** |  |





***

### createPayload

This function can be used to create custom JWT payloads

```php
protected createPayload(mixed $client_id, mixed $user_id, string $scope = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | - Client identifier related to the access token. |
| `$user_id` | **mixed** | - User ID associated with the access token |
| `$scope` | **string** | - (optional) Scopes to be stored in space-separated string. |


**Return Value:**

- The access token




***


## Inherited methods


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
> Automatically generated on 2025-03-18
