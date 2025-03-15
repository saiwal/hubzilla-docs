***

# AuthorizeControllerInterface

This controller is called when a user should be authorized
 by an authorization server.  As OAuth2 does not handle
 authorization directly, this controller ensures the request is valid, but
 requires the application to determine the value of $is_authorized

 @code
$user_id = $this->somehowDetermineUserId();
$is_authorized = $this->somehowDetermineUserAuthorization();
$response = new OAuth2\Response();
$authorizeController->handleAuthorizeRequest(
    OAuth2\Request::createFromGlobals(),
    $response,
    $is_authorized,
    $user_id
);
$response->send();

* Full name: `\OAuth2\Controller\AuthorizeControllerInterface`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`RESPONSE_TYPE_AUTHORIZATION_CODE`|public|string|&#039;code&#039;|
|`RESPONSE_TYPE_ACCESS_TOKEN`|public| |&#039;token&#039;|

## Methods


### handleAuthorizeRequest

Handle the OAuth request

```php
public handleAuthorizeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, mixed $is_authorized, null $user_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |
| `$is_authorized` | **mixed** |  |
| `$user_id` | **null** |  |





***

### validateAuthorizeRequest



```php
public validateAuthorizeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***


***
> Automatically generated on 2025-03-15
