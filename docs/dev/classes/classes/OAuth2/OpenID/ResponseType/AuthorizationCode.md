
# AuthorizationCode





* Full name: `\OAuth2\OpenID\ResponseType\AuthorizationCode`
* Parent class: [`\OAuth2\ResponseType\AuthorizationCode`](../../ResponseType/AuthorizationCode.md)
* This class implements:
[`\OAuth2\OpenID\ResponseType\AuthorizationCodeInterface`](./AuthorizationCodeInterface.md)




## Methods


### __construct

Constructor

```php
public __construct(\OAuth2\OpenID\Storage\AuthorizationCodeInterface $storage, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\OpenID\Storage\AuthorizationCodeInterface** |  |
| `$config` | **array** |  |





***

### getAuthorizeResponse



```php
public getAuthorizeResponse(mixed $params, null $user_id = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **mixed** |  |
| `$user_id` | **null** |  |





***

### createAuthorizationCode

Handle the creation of the authorization code.

```php
public createAuthorizationCode(mixed $client_id, mixed $user_id, string $redirect_uri, string $scope = null, string $id_token = null, mixed $code_challenge = null, mixed $code_challenge_method = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | - Client identifier related to the authorization code |
| `$user_id` | **mixed** | - User ID associated with the authorization code |
| `$redirect_uri` | **string** | - An absolute URI to which the authorization server will redirect the<br />user-agent to when the end-user authorization step is completed. |
| `$scope` | **string** | - OPTIONAL Scopes to be stored in space-separated string. |
| `$id_token` | **string** | - OPTIONAL The OpenID Connect id_token. |
| `$code_challenge` | **mixed** |  |
| `$code_challenge_method` | **mixed** |  |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4 - 

***


## Inherited methods


### __construct



```php
public __construct(\OAuth2\Storage\AuthorizationCodeInterface $storage, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\AuthorizationCodeInterface** |  |
| `$config` | **array** |  |





***

### getAuthorizeResponse



```php
public getAuthorizeResponse(mixed $params, mixed $user_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **mixed** |  |
| `$user_id` | **mixed** |  |





***

### createAuthorizationCode

Handle the creation of the authorization code.

```php
public createAuthorizationCode(mixed $client_id, mixed $user_id, mixed $redirect_uri, mixed $scope = null, mixed $code_challenge = null, mixed $code_challenge_method = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier related to the authorization code |
| `$user_id` | **mixed** | <br />User ID associated with the authorization code |
| `$redirect_uri` | **mixed** | <br />An absolute URI to which the authorization server will redirect the<br />user-agent to when the end-user authorization step is completed. |
| `$scope` | **mixed** | <br />(optional) Scopes to be stored in space-separated string. |
| `$code_challenge` | **mixed** |  |
| `$code_challenge_method` | **mixed** |  |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4 - 

***

### enforceRedirect



```php
public enforceRedirect(): true
```









**Return Value:**

if the grant type requires a redirect_uri, FALSE if not




***

### generateAuthorizationCode

Generates an unique auth code.

```php
protected generateAuthorizationCode(): \OAuth2\ResponseType\An
```

Implementing classes may want to override this function to implement
other auth code generation schemes.







**Return Value:**

unique auth code.




***


***
> Automatically generated on 2025-03-15
