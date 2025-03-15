
# AuthorizeController





* Full name: `\OAuth2\Controller\AuthorizeController`
* This class implements:
[`\OAuth2\Controller\AuthorizeControllerInterface`](./AuthorizeControllerInterface.md)

**See Also:**

* \OAuth2\Controller\AuthorizeControllerInterface - 



## Properties


### scope



```php
private string $scope
```






***

### state



```php
private int $state
```






***

### client_id



```php
private mixed $client_id
```






***

### redirect_uri



```php
private string $redirect_uri
```






***

### response_type

The response type

```php
private string $response_type
```






***

### clientStorage



```php
protected \OAuth2\Storage\ClientInterface $clientStorage
```






***

### responseTypes



```php
protected array $responseTypes
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

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



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
