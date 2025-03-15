
# ResourceControllerInterface

This controller is called when a "resource" is requested.

call verifyResourceRequest in order to determine if the request
contains a valid token.

* Full name: `\OAuth2\Controller\ResourceControllerInterface`



## Methods


### verifyResourceRequest

Verify the resource request

```php
public verifyResourceRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, string $scope = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |
| `$scope` | **string** |  |





***

### getAccessTokenData

Get access token data.

```php
public getAccessTokenData(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |





***


***
> Automatically generated on 2025-03-15
