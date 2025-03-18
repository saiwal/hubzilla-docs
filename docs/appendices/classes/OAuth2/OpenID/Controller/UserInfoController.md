
# UserInfoController





* Full name: `\OAuth2\OpenID\Controller\UserInfoController`
* Parent class: [`\OAuth2\Controller\ResourceController`](../../Controller/ResourceController.md)
* This class implements:
[`\OAuth2\OpenID\Controller\UserInfoControllerInterface`](./UserInfoControllerInterface.md)

**See Also:**

* \OAuth2\OpenID\Controller\OAuth2\Controller\UserInfoControllerInterface - 



## Properties


### userClaimsStorage



```php
protected \OAuth2\OpenID\Storage\UserClaimsInterface $userClaimsStorage
```






***

## Methods


### __construct

Constructor

```php
public __construct(\OAuth2\TokenType\TokenTypeInterface $tokenType, \OAuth2\Storage\AccessTokenInterface $tokenStorage, \OAuth2\OpenID\Storage\UserClaimsInterface $userClaimsStorage, array $config = array(), \OAuth2\ScopeInterface $scopeUtil = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokenType` | **\OAuth2\TokenType\TokenTypeInterface** |  |
| `$tokenStorage` | **\OAuth2\Storage\AccessTokenInterface** |  |
| `$userClaimsStorage` | **\OAuth2\OpenID\Storage\UserClaimsInterface** |  |
| `$config` | **array** |  |
| `$scopeUtil` | **\OAuth2\ScopeInterface** |  |





***

### handleUserInfoRequest

Handle the user info request

```php
public handleUserInfoRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***


## Inherited methods


### __construct

Constructor

```php
public __construct(\OAuth2\TokenType\TokenTypeInterface $tokenType, \OAuth2\Storage\AccessTokenInterface $tokenStorage, array $config = array(), \OAuth2\ScopeInterface $scopeUtil = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokenType` | **\OAuth2\TokenType\TokenTypeInterface** |  |
| `$tokenStorage` | **\OAuth2\Storage\AccessTokenInterface** |  |
| `$config` | **array** |  |
| `$scopeUtil` | **\OAuth2\ScopeInterface** |  |





***

### verifyResourceRequest

Verify the resource request

```php
public verifyResourceRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, null $scope = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |
| `$scope` | **null** |  |





***

### getAccessTokenData

Get access token data.

```php
public getAccessTokenData(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***

### getToken

convenience method to allow retrieval of the token.

```php
public getToken(): array
```












***


***
> Automatically generated on 2025-03-18
