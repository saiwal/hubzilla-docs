
# TokenControllerInterface

This controller is called when a token is being requested.

it is called to handle all grant types the application supports.
It also validates the client's credentials

* Full name: `\OAuth2\Controller\TokenControllerInterface`



## Methods


### handleTokenRequest

Handle the token request

```php
public handleTokenRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - The current http request |
| `$response` | **\OAuth2\ResponseInterface** | - An instance of OAuth2\ResponseInterface to contain the response data |





***

### grantAccessToken

Grant or deny a requested access token.

```php
public grantAccessToken(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```

This would be called from the "/token" endpoint as defined in the spec.
You can call your endpoint whatever you want.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object to grant access token |
| `$response` | **\OAuth2\ResponseInterface** | - Response object |





***


***
> Automatically generated on 2025-03-18
