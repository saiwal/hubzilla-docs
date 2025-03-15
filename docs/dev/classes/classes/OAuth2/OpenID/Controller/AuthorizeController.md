
# AuthorizeController





* Full name: `\OAuth2\OpenID\Controller\AuthorizeController`
* Parent class: [`\OAuth2\Controller\AuthorizeController`](../../Controller/AuthorizeController.md)
* This class implements:
[`\OAuth2\OpenID\Controller\AuthorizeControllerInterface`](./AuthorizeControllerInterface.md)

**See Also:**

* \OAuth2\OpenID\Controller\OAuth2\Controller\AuthorizeControllerInterface - 



## Properties


### nonce



```php
private mixed $nonce
```






***

### code_challenge



```php
protected mixed $code_challenge
```






***

### code_challenge_method



```php
protected mixed $code_challenge_method
```






***

## Methods


### setNotAuthorizedResponse

Set not authorized response

```php
protected setNotAuthorizedResponse(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, string $redirect_uri, null $user_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |
| `$redirect_uri` | **string** |  |
| `$user_id` | **null** |  |





***

### buildAuthorizeParameters

We have made this protected so this class can be extended to add/modify
these parameters

```php
protected buildAuthorizeParameters(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, mixed $user_id): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |
| `$user_id` | **mixed** |  |





***

### validateAuthorizeRequest

Validate the OAuth request

```php
public validateAuthorizeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***

### getValidResponseTypes

Array of valid response types

```php
protected getValidResponseTypes(): array
```












***

### needsIdToken

Returns whether the current request needs to generate an id token.

```php
public needsIdToken(string $request_scope): bool
```

ID Tokens are a part of the OpenID Connect specification, so this
method checks whether OpenID Connect is enabled in the server settings
and whether the openid scope was requested.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request_scope` | **string** | - A space-separated string of scopes. |


**Return Value:**

- TRUE if an id token is needed, FALSE otherwise.




***

### getNonce



```php
public getNonce(): mixed
```












***


## Inherited methods


### __construct

Constructor

```php
public __construct(\OAuth2\Storage\ClientInterface $clientStorage, array $responseTypes = array(), array $config = array(), \OAuth2\ScopeInterface $scopeUtil = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clientStorage` | **\OAuth2\Storage\ClientInterface** | REQUIRED Instance of OAuth2\Storage\ClientInterface to retrieve client information |
| `$responseTypes` | **array** | OPTIONAL Array of OAuth2\ResponseType\ResponseTypeInterface objects.  Valid array<br />keys are &quot;code&quot; and &quot;token&quot; |
| `$config` | **array** | OPTIONAL Configuration options for the server: |
| `$scopeUtil` | **\OAuth2\ScopeInterface** | OPTIONAL Instance of OAuth2\ScopeInterface to validate the requested scope |





***

### handleAuthorizeRequest

Handle the authorization request

```php
public handleAuthorizeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, bool $is_authorized, mixed $user_id = null): mixed|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |
| `$is_authorized` | **bool** |  |
| `$user_id` | **mixed** |  |




**Throws:**

- [`InvalidArgumentException`](../../../InvalidArgumentException.md)



***

### setNotAuthorizedResponse

Set not authorized response

```php
protected setNotAuthorizedResponse(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, string $redirect_uri, mixed $user_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |
| `$redirect_uri` | **string** |  |
| `$user_id` | **mixed** |  |





***

### buildAuthorizeParameters

We have made this protected so this class can be extended to add/modify
these parameters

```php
protected buildAuthorizeParameters(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response, mixed $user_id): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |
| `$user_id` | **mixed** |  |





***

### validateAuthorizeRequest

Validate the OAuth request

```php
public validateAuthorizeRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***

### buildUri

Build the absolute URI based on supplied URI and parameters.

```php
private buildUri(string $uri, array $params): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** | An absolute URI. |
| `$params` | **array** | Parameters to be append as GET. |


**Return Value:**


An absolute URI with supplied parameters.




***

### getValidResponseTypes



```php
protected getValidResponseTypes(): mixed
```












***

### validateRedirectUri

Internal method for validating redirect URI supplied

```php
protected validateRedirectUri(string $inputUri, string $registeredUriString): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inputUri` | **string** | The submitted URI to be validated |
| `$registeredUriString` | **string** | The allowed URI(s) to validate against.  Can be a space-delimited string of URIs to<br />allow for multiple URIs |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-3.1.2 - 

***

### getScope

Convenience method to access the scope

```php
public getScope(): string
```












***

### getState

Convenience method to access the state

```php
public getState(): int
```












***

### getClientId

Convenience method to access the client id

```php
public getClientId(): mixed
```












***

### getRedirectUri

Convenience method to access the redirect url

```php
public getRedirectUri(): string
```












***

### getResponseType

Convenience method to access the response type

```php
public getResponseType(): string
```












***


***
> Automatically generated on 2025-03-15
