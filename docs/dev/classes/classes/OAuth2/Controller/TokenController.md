***

# TokenController





* Full name: `\OAuth2\Controller\TokenController`
* This class implements:
[`\OAuth2\Controller\TokenControllerInterface`](./TokenControllerInterface.md)

**See Also:**

* \OAuth2\Controller\TokenControllerInterface - 



## Properties


### accessToken



```php
protected \OAuth2\ResponseType\AccessTokenInterface $accessToken
```






***

### grantTypes



```php
protected \OAuth2\GrantType\GrantTypeInterface[] $grantTypes
```






***

### clientAssertionType



```php
protected \OAuth2\ClientAssertionType\ClientAssertionTypeInterface $clientAssertionType
```






***

### scopeUtil



```php
protected \OAuth2\ScopeInterface $scopeUtil
```






***

### clientStorage



```php
protected \OAuth2\Storage\ClientInterface $clientStorage
```






***

## Methods


### __construct

Constructor

```php
public __construct(\OAuth2\ResponseType\AccessTokenInterface $accessToken, \OAuth2\Storage\ClientInterface $clientStorage, array $grantTypes = array(), \OAuth2\ClientAssertionType\ClientAssertionTypeInterface $clientAssertionType = null, \OAuth2\ScopeInterface $scopeUtil = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$accessToken` | **\OAuth2\ResponseType\AccessTokenInterface** |  |
| `$clientStorage` | **\OAuth2\Storage\ClientInterface** |  |
| `$grantTypes` | **array** |  |
| `$clientAssertionType` | **\OAuth2\ClientAssertionType\ClientAssertionTypeInterface** |  |
| `$scopeUtil` | **\OAuth2\ScopeInterface** |  |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### handleTokenRequest

Handle the token request.

```php
public handleTokenRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object to grant access token |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |





***

### grantAccessToken

Grant or deny a requested access token.

```php
public grantAccessToken(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool|null|array
```

This would be called from the "/token" endpoint as defined in the spec.
You can call your endpoint whatever you want.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object to grant access token |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)

- [`LogicException`](../../LogicException.md)



**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4 - * http://tools.ietf.org/html/rfc6749#section-10.6 - * http://tools.ietf.org/html/rfc6749#section-4.1.3 - 

***

### addGrantType

Add grant type

```php
public addGrantType(\OAuth2\GrantType\GrantTypeInterface $grantType, string|null $identifier = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$grantType` | **\OAuth2\GrantType\GrantTypeInterface** | - the grant type to add for the specified identifier |
| `$identifier` | **string&#124;null** | - a string passed in as &quot;grant_type&quot; in the response that will call this grantType |





***

### handleRevokeRequest



```php
public handleRevokeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***

### revokeToken

Revoke a refresh or access token. Returns true on success and when tokens are invalid

```php
public revokeToken(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool|null
```

Note: invalid tokens do not cause an error response since the client
cannot handle such an error in a reasonable way.  Moreover, the
purpose of the revocation request, invalidating the particular token,
is already achieved.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |




**Throws:**

- [`RuntimeException`](../../RuntimeException.md)



***


***
> Automatically generated on 2025-03-15
