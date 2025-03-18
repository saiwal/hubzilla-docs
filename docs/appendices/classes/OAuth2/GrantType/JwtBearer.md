
# JwtBearer

The JWT bearer authorization grant implements JWT (JSON Web Tokens) as a grant type per the IETF draft.



* Full name: `\OAuth2\GrantType\JwtBearer`
* This class implements:
[`\OAuth2\GrantType\GrantTypeInterface`](./GrantTypeInterface.md), [`\OAuth2\ClientAssertionType\ClientAssertionTypeInterface`](../ClientAssertionType/ClientAssertionTypeInterface.md)

**See Also:**

* http://tools.ietf.org/html/draft-ietf-oauth-jwt-bearer-04#section-4 - 



## Properties


### jwt



```php
private $jwt
```






***

### storage



```php
protected $storage
```






***

### audience



```php
protected $audience
```






***

### jwtUtil



```php
protected $jwtUtil
```






***

### allowedAlgorithms



```php
protected $allowedAlgorithms
```






***

## Methods


### __construct

Creates an instance of the JWT bearer grant type.

```php
public __construct(\OAuth2\Storage\JwtBearerInterface $storage, string $audience, \OAuth2\Encryption\EncryptionInterface|\OAuth2\GrantType\JWT $jwtUtil = null, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\JwtBearerInterface** | - A valid storage interface that implements storage hooks for the JWT<br />bearer grant type. |
| `$audience` | **string** | - The audience to validate the token against. This is usually the full<br />URI of the OAuth token requests endpoint. |
| `$jwtUtil` | **\OAuth2\Encryption\EncryptionInterface&#124;\OAuth2\GrantType\JWT** | - OPTONAL The class used to decode, encode and verify JWTs. |
| `$config` | **array** |  |





***

### getQueryStringIdentifier

Returns the grant_type get parameter to identify the grant type request as JWT bearer authorization grant.

```php
public getQueryStringIdentifier(): string
```









**Return Value:**

- The string identifier for grant_type.




**See Also:**

* \OAuth2\GrantType\GrantTypeInterface::getQueryStringIdentifier() - 

***

### validateRequest

Validates the data from the decoded JWT.

```php
public validateRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool|mixed|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |


**Return Value:**

TRUE if the JWT request is valid and can be decoded. Otherwise, FALSE is returned.@see GrantTypeInterface::getTokenData()




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
public getScope(): null
```












***

### createAccessToken

Creates an access token that is NOT associated with a refresh token.

```php
public createAccessToken(\OAuth2\ResponseType\AccessTokenInterface $accessToken, mixed $client_id, mixed $user_id, string $scope): array
```

If a subject (sub) the name of the user/account we are accessing data on behalf of.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$accessToken` | **\OAuth2\ResponseType\AccessTokenInterface** |  |
| `$client_id` | **mixed** | - client identifier related to the access token. |
| `$user_id` | **mixed** | - user id associated with the access token |
| `$scope` | **string** | - scopes to be stored in space-separated string. |





**See Also:**

* \OAuth2\GrantType\GrantTypeInterface::createAccessToken() - 

***


***
> Automatically generated on 2025-03-18
