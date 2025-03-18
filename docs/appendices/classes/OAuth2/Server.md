
# Server

Server class for OAuth2
This class serves as a convience class which wraps the other Controller classes



* Full name: `\OAuth2\Server`
* This class implements:
[`\OAuth2\Controller\ResourceControllerInterface`](./Controller/ResourceControllerInterface.md), [`\OAuth2\Controller\AuthorizeControllerInterface`](./Controller/AuthorizeControllerInterface.md), [`\OAuth2\Controller\TokenControllerInterface`](./Controller/TokenControllerInterface.md), [`\OAuth2\OpenID\Controller\UserInfoControllerInterface`](./OpenID/Controller/UserInfoControllerInterface.md)

**See Also:**

* \OAuth2\Controller\ResourceController - 
* \OAuth2\Controller\AuthorizeController - 
* \OAuth2\Controller\TokenController - 



## Properties


### response



```php
protected \OAuth2\ResponseInterface $response
```






***

### config



```php
protected array $config
```






***

### storages



```php
protected array $storages
```






***

### authorizeController



```php
protected \OAuth2\Controller\AuthorizeControllerInterface $authorizeController
```






***

### tokenController



```php
protected \OAuth2\Controller\TokenControllerInterface $tokenController
```






***

### resourceController



```php
protected \OAuth2\Controller\ResourceControllerInterface $resourceController
```






***

### userInfoController



```php
protected \OAuth2\OpenID\Controller\UserInfoControllerInterface $userInfoController
```






***

### grantTypes



```php
protected array $grantTypes
```






***

### responseTypes



```php
protected array $responseTypes
```






***

### tokenType



```php
protected \OAuth2\TokenType\TokenTypeInterface $tokenType
```






***

### scopeUtil



```php
protected \OAuth2\ScopeInterface $scopeUtil
```






***

### clientAssertionType



```php
protected \OAuth2\ClientAssertionType\ClientAssertionTypeInterface $clientAssertionType
```






***

### storageMap



```php
protected array $storageMap
```






***

### responseTypeMap



```php
protected array $responseTypeMap
```






***

## Methods


### __construct



```php
public __construct(mixed $storage = array(), array $config = array(), array $grantTypes = array(), array $responseTypes = array(), \OAuth2\TokenType\TokenTypeInterface $tokenType = null, \OAuth2\ScopeInterface $scopeUtil = null, \OAuth2\ClientAssertionType\ClientAssertionTypeInterface $clientAssertionType = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **mixed** | (array or OAuth2\Storage) - single object or array of objects implementing the<br />required storage types (ClientCredentialsInterface and AccessTokenInterface as a minimum) |
| `$config` | **array** | specify a different token lifetime, token header name, etc |
| `$grantTypes` | **array** | An array of OAuth2\GrantType\GrantTypeInterface to use for granting access tokens |
| `$responseTypes` | **array** | Response types to use. array keys should be &quot;code&quot; and &quot;token&quot; for<br />Access Token and Authorization Code response types |
| `$tokenType` | **\OAuth2\TokenType\TokenTypeInterface** | The token type object to use. Valid token types are &quot;bearer&quot; and &quot;mac&quot; |
| `$scopeUtil` | **\OAuth2\ScopeInterface** | The scope utility class to use to validate scope |
| `$clientAssertionType` | **\OAuth2\ClientAssertionType\ClientAssertionTypeInterface** | The method in which to verify the client identity.  Default is HttpBasic |





***

### getAuthorizeController



```php
public getAuthorizeController(): \OAuth2\Controller\AuthorizeControllerInterface
```












***

### getTokenController



```php
public getTokenController(): \OAuth2\Controller\TokenController
```












***

### getResourceController



```php
public getResourceController(): \OAuth2\Controller\ResourceControllerInterface
```












***

### getUserInfoController



```php
public getUserInfoController(): \OAuth2\OpenID\Controller\UserInfoControllerInterface
```












***

### setAuthorizeController



```php
public setAuthorizeController(\OAuth2\Controller\AuthorizeControllerInterface $authorizeController): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$authorizeController` | **\OAuth2\Controller\AuthorizeControllerInterface** |  |





***

### setTokenController



```php
public setTokenController(\OAuth2\Controller\TokenControllerInterface $tokenController): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokenController` | **\OAuth2\Controller\TokenControllerInterface** |  |





***

### setResourceController



```php
public setResourceController(\OAuth2\Controller\ResourceControllerInterface $resourceController): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$resourceController` | **\OAuth2\Controller\ResourceControllerInterface** |  |





***

### setUserInfoController



```php
public setUserInfoController(\OAuth2\OpenID\Controller\UserInfoControllerInterface $userInfoController): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$userInfoController` | **\OAuth2\OpenID\Controller\UserInfoControllerInterface** |  |





***

### handleUserInfoRequest

Return claims about the authenticated end-user.

```php
public handleUserInfoRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): \OAuth2\ResponseInterface
```

This would be called from the "/UserInfo" endpoint as defined in the spec.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object to grant access token |
| `$response` | **\OAuth2\ResponseInterface** | - Response object containing error messages (failure) or user claims (success) |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)

- [`LogicException`](../LogicException.md)



**See Also:**

* http://openid.net/specs/openid-connect-core-1_0.html#UserInfo - 

***

### handleTokenRequest

Grant or deny a requested access token.

```php
public handleTokenRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): \OAuth2\ResponseInterface
```

This would be called from the "/token" endpoint as defined in the spec.
Obviously, you can call your endpoint whatever you want.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object to grant access token |
| `$response` | **\OAuth2\ResponseInterface** | - Response object containing error messages (failure) or access token (success) |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)

- [`LogicException`](../LogicException.md)



**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4 - * http://tools.ietf.org/html/rfc6749#section-10.6 - * http://tools.ietf.org/html/rfc6749#section-4.1.3 - 

***

### grantAccessToken

Grant or deny a requested access token.

```php
public grantAccessToken(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object to grant access token |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |





***

### handleRevokeRequest

Handle a revoke token request
This would be called from the "/revoke" endpoint as defined in the draft Token Revocation spec

```php
public handleRevokeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): \OAuth2\Response|\OAuth2\ResponseInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





**See Also:**

* https://tools.ietf.org/html/rfc7009#section-2 - 

***

### handleAuthorizeRequest

Redirect the user appropriately after approval.

```php
public handleAuthorizeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, bool $is_authorized, mixed $user_id = null): \OAuth2\ResponseInterface
```

After the user has approved or denied the resource request the
authorization server should call this function to redirect the user
appropriately.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - The request should have the follow parameters set in the querystring:<br />- response_type: The requested response: an access token, an authorization code, or both.<br />- client_id: The client identifier as described in Section 2.<br />- redirect_uri: An absolute URI to which the authorization server will redirect the user-agent to when the<br />  end-user authorization step is completed.<br />- scope: (optional) The scope of the resource request expressed as a list of space-delimited strings.<br />- state: (optional) An opaque value used by the client to maintain state between the request and callback. |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |
| `$is_authorized` | **bool** | - TRUE or FALSE depending on whether the user authorized the access. |
| `$user_id` | **mixed** | - Identifier of user who authorized the client |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4 - 

***

### validateAuthorizeRequest

Pull the authorization request data out of the HTTP request.

```php
public validateAuthorizeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): bool
```

- The redirect_uri is OPTIONAL as per draft 20. But your implementation can enforce it
  by setting $config['enforce_redirect'] to true.
- The state is OPTIONAL but recommended to enforce CSRF. Draft 21 states, however, that
  CSRF protection is MANDATORY. You can enforce this by setting the $config['enforce_state'] to true.

The draft specifies that the parameters should be retrieved from GET, override the Response
object to change this






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |


**Return Value:**



The authorization parameters so the authorization server can prompt
the user for approval if valid.




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4.1.1 - * http://tools.ietf.org/html/rfc6749#section-10.12 - 

***

### verifyResourceRequest

Verify the resource request

```php
public verifyResourceRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null, string $scope = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |
| `$scope` | **string** | - Scope |





***

### getAccessTokenData

Get access token data.

```php
public getAccessTokenData(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |





***

### addGrantType



```php
public addGrantType(\OAuth2\GrantType\GrantTypeInterface $grantType, mixed $identifier = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$grantType` | **\OAuth2\GrantType\GrantTypeInterface** |  |
| `$identifier` | **mixed** |  |





***

### addStorage

Set a storage object for the server

```php
public addStorage(object $storage, mixed $key = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **object** | - An object implementing one of the Storage interfaces |
| `$key` | **mixed** | - If null, the storage is set to the key of each storage interface it implements |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



**See Also:**

* \OAuth2\storageMap - 

***

### addResponseType



```php
public addResponseType(\OAuth2\ResponseType\ResponseTypeInterface $responseType, mixed $key = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$responseType` | **\OAuth2\ResponseType\ResponseTypeInterface** |  |
| `$key` | **mixed** |  |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



***

### getScopeUtil



```php
public getScopeUtil(): \OAuth2\ScopeInterface
```












***

### setScopeUtil



```php
public setScopeUtil(\OAuth2\ScopeInterface $scopeUtil): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scopeUtil` | **\OAuth2\ScopeInterface** |  |





***

### createDefaultAuthorizeController



```php
protected createDefaultAuthorizeController(): \OAuth2\Controller\AuthorizeControllerInterface
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### createDefaultTokenController



```php
protected createDefaultTokenController(): \OAuth2\Controller\TokenControllerInterface
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### createDefaultResourceController



```php
protected createDefaultResourceController(): \OAuth2\Controller\ResourceControllerInterface
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### createDefaultUserInfoController



```php
protected createDefaultUserInfoController(): \OAuth2\OpenID\Controller\UserInfoControllerInterface
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### getDefaultTokenType



```php
protected getDefaultTokenType(): \OAuth2\TokenType\Bearer
```












***

### getDefaultResponseTypes



```php
protected getDefaultResponseTypes(): array
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### getDefaultGrantTypes



```php
protected getDefaultGrantTypes(): array
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### getAccessTokenResponseType



```php
protected getAccessTokenResponseType(): \OAuth2\ResponseType\AccessToken
```












***

### getIdTokenResponseType



```php
protected getIdTokenResponseType(): \OAuth2\OpenID\ResponseType\IdToken
```












***

### getIdTokenTokenResponseType



```php
protected getIdTokenTokenResponseType(): \OAuth2\OpenID\ResponseType\IdTokenToken
```












***

### createDefaultJwtAccessTokenStorage

For Resource Controller

```php
protected createDefaultJwtAccessTokenStorage(): \OAuth2\Storage\JwtAccessToken
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### createDefaultJwtAccessTokenResponseType

For Authorize and Token Controllers

```php
protected createDefaultJwtAccessTokenResponseType(): \OAuth2\ResponseType\JwtAccessToken
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### createDefaultAccessTokenResponseType



```php
protected createDefaultAccessTokenResponseType(): \OAuth2\ResponseType\AccessToken
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### createDefaultIdTokenResponseType



```php
protected createDefaultIdTokenResponseType(): \OAuth2\OpenID\ResponseType\IdToken
```











**Throws:**

- [`LogicException`](../LogicException.md)



***

### createDefaultIdTokenTokenResponseType



```php
protected createDefaultIdTokenTokenResponseType(): \OAuth2\OpenID\ResponseType\IdTokenToken
```












***

### validateOpenIdConnect



```php
protected validateOpenIdConnect(): mixed
```











**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



***

### normalizeResponseType



```php
protected normalizeResponseType(string $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getResponse



```php
public getResponse(): mixed
```












***

### getStorages



```php
public getStorages(): array
```












***

### getStorage



```php
public getStorage(string $name): object|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getGrantTypes



```php
public getGrantTypes(): array
```












***

### getGrantType



```php
public getGrantType(string $name): object|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getResponseTypes



```php
public getResponseTypes(): array
```












***

### getResponseType



```php
public getResponseType(string $name): object|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getTokenType



```php
public getTokenType(): \OAuth2\TokenType\TokenTypeInterface
```












***

### getClientAssertionType



```php
public getClientAssertionType(): \OAuth2\ClientAssertionType\ClientAssertionTypeInterface
```












***

### setConfig



```php
public setConfig(string $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### getConfig



```php
public getConfig(string $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$default` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
