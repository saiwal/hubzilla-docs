
# ClientCredentials

Validate a client via Http Basic authentication



* Full name: `\OAuth2\GrantType\ClientCredentials`
* Parent class: [`\OAuth2\ClientAssertionType\HttpBasic`](../ClientAssertionType/HttpBasic.md)
* This class implements:
[`\OAuth2\GrantType\GrantTypeInterface`](./GrantTypeInterface.md)

**See Also:**

* \OAuth2\ClientAssertionType\HttpBasic - 



## Properties


### clientData



```php
private array $clientData
```






***

## Methods


### __construct

Config array $config should look as follows:

```php
public __construct(\OAuth2\Storage\ClientCredentialsInterface $storage, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\ClientCredentialsInterface** |  |
| `$config` | **array** |  |





***

### getQueryStringIdentifier

Get query string identifier

```php
public getQueryStringIdentifier(): string
```












***

### getScope

Get scope

```php
public getScope(): string|null
```












***

### getUserId

Get user id

```php
public getUserId(): mixed
```












***

### createAccessToken

Create access token

```php
public createAccessToken(\OAuth2\ResponseType\AccessTokenInterface $accessToken, mixed $client_id, mixed $user_id, string $scope): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$accessToken` | **\OAuth2\ResponseType\AccessTokenInterface** |  |
| `$client_id` | **mixed** | - client identifier related to the access token. |
| `$user_id` | **mixed** | - user id associated with the access token |
| `$scope` | **string** | - scopes to be stored in space-separated string. |





***

### loadClientData



```php
private loadClientData(): mixed
```












***


## Inherited methods


### __construct

Config array $config should look as follows:

```php
public __construct(\OAuth2\Storage\ClientCredentialsInterface $storage, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\ClientCredentialsInterface** | Storage |
| `$config` | **array** | Configuration options for the server |





***

### validateRequest

Validate the OAuth request

```php
public validateRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |




**Throws:**

- [`LogicException`](../../LogicException.md)



***

### getClientId

Get the client id

```php
public getClientId(): mixed
```












***

### getClientCredentials

Internal function used to get the client credentials from HTTP basic
auth or POST data.

```php
public getClientCredentials(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): array|null
```

According to the spec (draft 20), the client_id can be provided in
the Basic Authorization header (recommended) or via GET/POST.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |


**Return Value:**

A list containing the client identifier and password, for example:




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-2.3.1 - 

***


***
> Automatically generated on 2025-03-15
