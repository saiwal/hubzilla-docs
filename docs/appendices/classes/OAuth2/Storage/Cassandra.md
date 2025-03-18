
# Cassandra

Cassandra storage for all storage types

To use, install "thobbs/phpcassa" via composer:
<code>
    composer require thobbs/phpcassa:dev-master
</code>

Once this is done, instantiate the connection:
<code>
    $cassandra = new \phpcassa\Connection\ConnectionPool('oauth2_server', array('127.0.0.1:9160'));
</code>

Then, register the storage client:
<code>
    $storage = new OAuth2\Storage\Cassandra($cassandra);
    $storage->setClientDetails($client_id, $client_secret, $redirect_uri);
</code>

* Full name: `\OAuth2\Storage\Cassandra`
* This class implements:
[`\OAuth2\Storage\AuthorizationCodeInterface`](./AuthorizationCodeInterface.md), [`\OAuth2\Storage\AccessTokenInterface`](./AccessTokenInterface.md), [`\OAuth2\Storage\ClientCredentialsInterface`](./ClientCredentialsInterface.md), [`\OAuth2\Storage\UserCredentialsInterface`](./UserCredentialsInterface.md), [`\OAuth2\Storage\RefreshTokenInterface`](./RefreshTokenInterface.md), [`\OAuth2\Storage\JwtBearerInterface`](./JwtBearerInterface.md), [`\OAuth2\Storage\ScopeInterface`](./ScopeInterface.md), [`\OAuth2\Storage\PublicKeyInterface`](./PublicKeyInterface.md), [`\OAuth2\OpenID\Storage\UserClaimsInterface`](../OpenID/Storage/UserClaimsInterface.md), [`\OAuth2\OpenID\Storage\AuthorizationCodeInterface`](../OpenID/Storage/AuthorizationCodeInterface.md)

**See Also:**

*  - test/lib/OAuth2/Storage/Bootstrap::getCassandraStorage



## Properties


### cache



```php
private $cache
```






***

### cassandra



```php
protected \phpcassa\Connection\ConnectionPool $cassandra
```






***

### config



```php
protected array $config
```






***

## Methods


### __construct

Cassandra Storage! uses phpCassa

```php
public __construct(\phpcassa\Connection\ConnectionPool|array $connection = array(), array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$connection` | **\phpcassa\Connection\ConnectionPool&#124;array** |  |
| `$config` | **array** |  |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### getValue



```php
protected getValue(mixed $key): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### setValue



```php
protected setValue(mixed $key, mixed $value, int $expire): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |
| `$value` | **mixed** |  |
| `$expire` | **int** |  |





***

### expireValue



```php
protected expireValue(mixed $key): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### getAuthorizationCode

Fetch authorization code data (probably the most common grant type).

```php
public getAuthorizationCode(string $code): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |





***

### setAuthorizationCode

Take the provided authorization code values and store them somewhere.

```php
public setAuthorizationCode(string $authorization_code, mixed $client_id, mixed $user_id, string $redirect_uri, int $expires, string $scope = null, string $id_token = null, mixed $code_challenge = null, mixed $code_challenge_method = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$authorization_code` | **string** |  |
| `$client_id` | **mixed** |  |
| `$user_id` | **mixed** |  |
| `$redirect_uri` | **string** |  |
| `$expires` | **int** |  |
| `$scope` | **string** |  |
| `$id_token` | **string** |  |
| `$code_challenge` | **mixed** |  |
| `$code_challenge_method` | **mixed** |  |





***

### expireAuthorizationCode

once an Authorization Code is used, it must be expired

```php
public expireAuthorizationCode(string $code): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |





***

### checkUserCredentials

Grant access tokens for basic user credentials.

```php
public checkUserCredentials(string $username, string $password): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |





***

### checkPassword

plaintext passwords are bad!  Override this for your application

```php
protected checkPassword(array $user, string $password): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$user` | **array** |  |
| `$password` | **string** |  |





***

### hashPassword



```php
protected hashPassword(mixed $password): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$password` | **mixed** |  |





***

### getUserDetails



```php
public getUserDetails(string $username): array|bool|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |





***

### getUser



```php
public getUser(string $username): array|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |





***

### setUser



```php
public setUser(string $username, string $password, string $first_name = null, string $last_name = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |
| `$first_name` | **string** |  |
| `$last_name` | **string** |  |





***

### checkClientCredentials

Make sure that the client credentials is valid.

```php
public checkClientCredentials(mixed $client_id, string $client_secret = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$client_secret` | **string** |  |





***

### isPublicClient

Determine if the client is a "public" client, and therefore
does not require passing credentials for certain grant types

```php
public isPublicClient(mixed $client_id): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getClientDetails

Get client details corresponding client_id.

```php
public getClientDetails(mixed $client_id): array|bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### setClientDetails



```php
public setClientDetails(mixed $client_id, null $client_secret = null, null $redirect_uri = null, null $grant_types = null, null $scope = null, null $user_id = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$client_secret` | **null** |  |
| `$redirect_uri` | **null** |  |
| `$grant_types` | **null** |  |
| `$scope` | **null** |  |
| `$user_id` | **null** |  |





***

### checkRestrictedGrantType

Check restricted grant types of corresponding client identifier.

```php
public checkRestrictedGrantType(mixed $client_id, mixed $grant_type): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$grant_type` | **mixed** |  |





***

### getRefreshToken

Grant refresh access tokens.

```php
public getRefreshToken(mixed $refresh_token): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **mixed** |  |





***

### setRefreshToken

Take the provided refresh token values and store them somewhere.

```php
public setRefreshToken(mixed $refresh_token, mixed $client_id, mixed $user_id, mixed $expires, null $scope = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **mixed** |  |
| `$client_id` | **mixed** |  |
| `$user_id` | **mixed** |  |
| `$expires` | **mixed** |  |
| `$scope` | **null** |  |





***

### unsetRefreshToken

Expire a used refresh token.

```php
public unsetRefreshToken(mixed $refresh_token): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **mixed** |  |





***

### getAccessToken

Look up the supplied oauth_token from storage.

```php
public getAccessToken(string $access_token): array|bool|mixed|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **string** |  |





***

### setAccessToken

Store the supplied access token values to storage.

```php
public setAccessToken(string $access_token, mixed $client_id, mixed $user_id, int $expires, null $scope = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **string** |  |
| `$client_id` | **mixed** |  |
| `$user_id` | **mixed** |  |
| `$expires` | **int** |  |
| `$scope` | **null** |  |





***

### unsetAccessToken



```php
public unsetAccessToken(mixed $access_token): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **mixed** |  |





***

### scopeExists

Check if the provided scope exists.

```php
public scopeExists(mixed $scope): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **mixed** |  |





***

### getDefaultScope

The default scope to use in the event the client
does not request one. By returning "false", a
request_error is returned by the server to force a
scope request by the client. By returning "null",
opt out of requiring scopes

```php
public getDefaultScope(null $client_id = null): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **null** |  |





***

### setScope



```php
public setScope(mixed $scope, null $client_id = null, string $type = &#039;supported&#039;): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **mixed** |  |
| `$client_id` | **null** |  |
| `$type` | **string** |  |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### getClientKey

Get the public key associated with a client_id

```php
public getClientKey(mixed $client_id, mixed $subject): bool|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$subject` | **mixed** |  |





***

### setClientKey



```php
public setClientKey(mixed $client_id, mixed $key, null $subject = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$key` | **mixed** |  |
| `$subject` | **null** |  |





***

### getClientScope

Get the scope associated with this client

```php
public getClientScope(mixed $client_id): bool|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getJti

Get a jti (JSON token identifier) by matching against the client_id, subject, audience and expiration.

```php
public getJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expiration, mixed $jti): \OAuth2\Storage\An
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$subject` | **mixed** |  |
| `$audience` | **mixed** |  |
| `$expiration` | **mixed** |  |
| `$jti` | **mixed** |  |


**Return Value:**

associative array as below, and return NULL if the jti does not exist.
- issuer: Stored client identifier.
- subject: Stored subject.
- audience: Stored audience.
- expires: Stored expiration in unix timestamp.
- jti: The stored jti.



**Throws:**

- [`Exception`](../../Exception.md)



***

### setJti

Store a used jti so that we can check against it to prevent replay attacks.

```php
public setJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expiration, mixed $jti): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$subject` | **mixed** |  |
| `$audience` | **mixed** |  |
| `$expiration` | **mixed** |  |
| `$jti` | **mixed** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### getPublicKey



```php
public getPublicKey(string $client_id = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **string** |  |





***

### getPrivateKey



```php
public getPrivateKey(string $client_id = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **string** |  |





***

### getEncryptionAlgorithm



```php
public getEncryptionAlgorithm(null $client_id = null): mixed|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **null** |  |





***

### getUserClaims

Return claims about the provided user id.

```php
public getUserClaims(mixed $user_id, string $claims): array|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$user_id` | **mixed** |  |
| `$claims` | **string** |  |





***

### getUserClaim



```php
protected getUserClaim(mixed $claim, mixed $userDetails): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$claim` | **mixed** |  |
| `$userDetails` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
