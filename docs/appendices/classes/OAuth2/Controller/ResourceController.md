
# ResourceController





* Full name: `\OAuth2\Controller\ResourceController`
* This class implements:
[`\OAuth2\Controller\ResourceControllerInterface`](./ResourceControllerInterface.md)

**See Also:**

* \OAuth2\Controller\ResourceControllerInterface - 



## Properties


### token



```php
private array $token
```






***

### tokenType



```php
protected \OAuth2\TokenType\TokenTypeInterface $tokenType
```






***

### tokenStorage



```php
protected \OAuth2\Storage\AccessTokenInterface $tokenStorage
```






***

### config



```php
protected array $config
```






***

### scopeUtil



```php
protected \OAuth2\ScopeInterface $scopeUtil
```






***

## Methods


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
