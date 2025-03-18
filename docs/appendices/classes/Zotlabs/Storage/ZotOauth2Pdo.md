
# ZotOauth2Pdo

Simple PDO storage for all storage types

NOTE: This class is meant to get users started
quickly. If your application requires further
customization, extend this class or create your own.

NOTE: Passwords are stored in plaintext, which is never
a good idea.  Be sure to override this for your application

* Full name: `\Zotlabs\Storage\ZotOauth2Pdo`
* Parent class: [`\OAuth2\Storage\Pdo`](../../OAuth2/Storage/Pdo.md)




## Methods


### getConfig



```php
public getConfig(): mixed
```












***


## Inherited methods


### __construct



```php
public __construct(mixed $connection, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$connection` | **mixed** |  |
| `$config` | **array** |  |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### checkClientCredentials

Make sure that the client credentials is valid.

```php
public checkClientCredentials(string $client_id, null|string $client_secret = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **string** |  |
| `$client_secret` | **null&#124;string** |  |





***

### isPublicClient

Determine if the client is a "public" client, and therefore
does not require passing credentials for certain grant types

```php
public isPublicClient(string $client_id): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **string** |  |





***

### getClientDetails

Get client details corresponding client_id.

```php
public getClientDetails(string $client_id): array|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **string** |  |





***

### setClientDetails



```php
public setClientDetails(string $client_id, null|string $client_secret = null, null|string $redirect_uri = null, null|array $grant_types = null, null|string $scope = null, null|string $user_id = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **string** |  |
| `$client_secret` | **null&#124;string** |  |
| `$redirect_uri` | **null&#124;string** |  |
| `$grant_types` | **null&#124;array** |  |
| `$scope` | **null&#124;string** |  |
| `$user_id` | **null&#124;string** |  |





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
public setAccessToken(string $access_token, mixed $client_id, mixed $user_id, int $expires, string $scope = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **string** |  |
| `$client_id` | **mixed** |  |
| `$user_id` | **mixed** |  |
| `$expires` | **int** |  |
| `$scope` | **string** |  |





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

### getAuthorizationCode

Fetch authorization code data (probably the most common grant type).

```php
public getAuthorizationCode(string $code): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |





***

### setAuthorizationCode

Take the provided authorization code values and store them somewhere.

```php
public setAuthorizationCode(string $code, mixed $client_id, mixed $user_id, string $redirect_uri, int $expires, string $scope = null, string $id_token = null, mixed $code_challenge = null, mixed $code_challenge_method = null): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |
| `$client_id` | **mixed** |  |
| `$user_id` | **mixed** |  |
| `$redirect_uri` | **string** |  |
| `$expires` | **int** |  |
| `$scope` | **string** |  |
| `$id_token` | **string** |  |
| `$code_challenge` | **mixed** |  |
| `$code_challenge_method` | **mixed** |  |





***

### setAuthorizationCodeWithIdToken



```php
private setAuthorizationCodeWithIdToken(string $code, mixed $client_id, mixed $user_id, string $redirect_uri, string $expires, string $scope = null, string $id_token = null, mixed $code_challenge = null, mixed $code_challenge_method = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |
| `$client_id` | **mixed** |  |
| `$user_id` | **mixed** |  |
| `$redirect_uri` | **string** |  |
| `$expires` | **string** |  |
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

### getUserDetails



```php
public getUserDetails(string $username): array|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |





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
protected getUserClaim(string $claim, array $userDetails): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$claim` | **string** |  |
| `$userDetails` | **array** |  |





***

### getRefreshToken

Grant refresh access tokens.

```php
public getRefreshToken(string $refresh_token): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **string** |  |





***

### setRefreshToken

Take the provided refresh token values and store them somewhere.

```php
public setRefreshToken(string $refresh_token, mixed $client_id, mixed $user_id, string $expires, string $scope = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **string** |  |
| `$client_id` | **mixed** |  |
| `$user_id` | **mixed** |  |
| `$expires` | **string** |  |
| `$scope` | **string** |  |





***

### unsetRefreshToken

Expire a used refresh token.

```php
public unsetRefreshToken(string $refresh_token): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **string** |  |





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

plaintext passwords are bad!  Override this for your application

```php
public setUser(string $username, string $password, string $firstName = null, string $lastName = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |
| `$firstName` | **string** |  |
| `$lastName` | **string** |  |





***

### scopeExists

Check if the provided scope exists.

```php
public scopeExists(string $scope): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **string** |  |





***

### getDefaultScope

The default scope to use in the event the client
does not request one. By returning "false", a
request_error is returned by the server to force a
scope request by the client. By returning "null",
opt out of requiring scopes

```php
public getDefaultScope(mixed $client_id = null): null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getClientKey

Get the public key associated with a client_id

```php
public getClientKey(mixed $client_id, mixed $subject): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$subject` | **mixed** |  |





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
public getJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expires, mixed $jti): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$subject` | **mixed** |  |
| `$audience` | **mixed** |  |
| `$expires` | **mixed** |  |
| `$jti` | **mixed** |  |





***

### setJti

Store a used jti so that we can check against it to prevent replay attacks.

```php
public setJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expires, mixed $jti): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$subject` | **mixed** |  |
| `$audience` | **mixed** |  |
| `$expires` | **mixed** |  |
| `$jti` | **mixed** |  |





***

### getPublicKey



```php
public getPublicKey(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getPrivateKey



```php
public getPrivateKey(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getEncryptionAlgorithm



```php
public getEncryptionAlgorithm(mixed $client_id = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getBuildSql

DDL to create OAuth2 database and tables for PDO storage

```php
public getBuildSql(string $dbName = &#039;oauth2_server_php&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dbName` | **string** |  |





**See Also:**

* https://github.com/dsquier/oauth2-server-php-mysql - 

***


***
> Automatically generated on 2025-03-18
