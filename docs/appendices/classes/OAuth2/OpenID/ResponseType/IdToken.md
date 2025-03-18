
# IdToken





* Full name: `\OAuth2\OpenID\ResponseType\IdToken`
* This class implements:
[`\OAuth2\OpenID\ResponseType\IdTokenInterface`](./IdTokenInterface.md)



## Properties


### userClaimsStorage



```php
protected \OAuth2\OpenID\Storage\UserClaimsInterface $userClaimsStorage
```






***

### publicKeyStorage



```php
protected \OAuth2\Storage\PublicKeyInterface $publicKeyStorage
```






***

### config



```php
protected array $config
```






***

### encryptionUtil



```php
protected \OAuth2\Encryption\EncryptionInterface $encryptionUtil
```






***

## Methods


### __construct

Constructor

```php
public __construct(\OAuth2\OpenID\Storage\UserClaimsInterface $userClaimsStorage, \OAuth2\Storage\PublicKeyInterface $publicKeyStorage, array $config = array(), \OAuth2\Encryption\EncryptionInterface $encryptionUtil = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$userClaimsStorage` | **\OAuth2\OpenID\Storage\UserClaimsInterface** |  |
| `$publicKeyStorage` | **\OAuth2\Storage\PublicKeyInterface** |  |
| `$config` | **array** |  |
| `$encryptionUtil` | **\OAuth2\Encryption\EncryptionInterface** |  |




**Throws:**

- [`LogicException`](../../../LogicException.md)



***

### getAuthorizeResponse



```php
public getAuthorizeResponse(array $params, null $userInfo = null): array|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** |  |
| `$userInfo` | **null** |  |





***

### createIdToken

Create id token

```php
public createIdToken(string $client_id, mixed $userInfo, mixed $nonce = null, mixed $userClaims = null, mixed $access_token = null): mixed|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **string** |  |
| `$userInfo` | **mixed** |  |
| `$nonce` | **mixed** |  |
| `$userClaims` | **mixed** |  |
| `$access_token` | **mixed** |  |





***

### createAtHash



```php
protected createAtHash(mixed $access_token, null $client_id = null): mixed|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **mixed** |  |
| `$client_id` | **null** |  |





***

### encodeToken



```php
protected encodeToken(array $token, null $client_id = null): mixed|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **array** |  |
| `$client_id` | **null** |  |





***

### getUserIdAndAuthTime



```php
private getUserIdAndAuthTime(mixed $userInfo): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$userInfo` | **mixed** |  |




**Throws:**

- [`LogicException`](../../../LogicException.md)



***


***
> Automatically generated on 2025-03-18
