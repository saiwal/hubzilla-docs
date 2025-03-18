
# JwtAccessToken





* Full name: `\OAuth2\Storage\JwtAccessToken`
* This class implements:
[`\OAuth2\Storage\JwtAccessTokenInterface`](./JwtAccessTokenInterface.md)



## Properties


### publicKeyStorage



```php
protected $publicKeyStorage
```






***

### tokenStorage



```php
protected $tokenStorage
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
public __construct(\OAuth2\Storage\OAuth2\Encryption\PublicKeyInterface $publicKeyStorage, \OAuth2\Storage\OAuth2\Storage\AccessTokenInterface $tokenStorage = null, \OAuth2\Storage\OAuth2\Encryption\EncryptionInterface $encryptionUtil = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$publicKeyStorage` | **\OAuth2\Storage\OAuth2\Encryption\PublicKeyInterface** | the public key encryption to use |
| `$tokenStorage` | **\OAuth2\Storage\OAuth2\Storage\AccessTokenInterface** | OPTIONAL persist the access token to another storage. This is useful if<br />you want to retain access token grant information somewhere, but<br />is not necessary when using this grant type. |
| `$encryptionUtil` | **\OAuth2\Storage\OAuth2\Encryption\EncryptionInterface** | OPTIONAL class to use for &quot;encode&quot; and &quot;decode&quot; functions. |





***

### getAccessToken

Look up the supplied oauth_token from storage.

```php
public getAccessToken(mixed $oauth_token): array|null
```

We need to retrieve access token data as we create and verify tokens.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oauth_token` | **mixed** | - oauth_token to be check with. |


**Return Value:**

- An associative array as below, and return NULL if the supplied oauth_token is invalid:




***

### setAccessToken

Store the supplied access token values to storage.

```php
public setAccessToken(mixed $oauth_token, mixed $client_id, mixed $user_id, mixed $expires, mixed $scope = null): mixed
```

We need to store access token data as we create and verify tokens.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oauth_token` | **mixed** | - oauth_token to be stored. |
| `$client_id` | **mixed** | - client identifier to be stored. |
| `$user_id` | **mixed** | - user identifier to be stored. |
| `$expires` | **mixed** | - expiration to be stored as a Unix timestamp. |
| `$scope` | **mixed** | - OPTIONAL Scopes to be stored in space-separated string. |





***

### unsetAccessToken



```php
public unsetAccessToken(mixed $access_token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **mixed** |  |





***

### convertJwtToOAuth2



```php
protected convertJwtToOAuth2(mixed $tokenData): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokenData` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
