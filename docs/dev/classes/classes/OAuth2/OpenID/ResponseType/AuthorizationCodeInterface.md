
# AuthorizationCodeInterface





* Full name: `\OAuth2\OpenID\ResponseType\AuthorizationCodeInterface`
* Parent interfaces: [`\OAuth2\ResponseType\AuthorizationCodeInterface`](../../ResponseType/AuthorizationCodeInterface.md)


## Methods


### createAuthorizationCode

Handle the creation of the authorization code.

```php
public createAuthorizationCode(mixed $client_id, mixed $user_id, string $redirect_uri, string $scope = null, string $id_token = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | - Client identifier related to the authorization code |
| `$user_id` | **mixed** | - User ID associated with the authorization code |
| `$redirect_uri` | **string** | - An absolute URI to which the authorization server will redirect the<br />user-agent to when the end-user authorization step is completed. |
| `$scope` | **string** | - OPTIONAL Scopes to be stored in space-separated string. |
| `$id_token` | **string** | - OPTIONAL The OpenID Connect id_token. |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4 - 

***


## Inherited methods


### getAuthorizeResponse



```php
public getAuthorizeResponse(array $params, mixed $user_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** |  |
| `$user_id` | **mixed** |  |





***

### enforceRedirect



```php
public enforceRedirect(): true
```









**Return Value:**

if the grant type requires a redirect_uri, FALSE if not




***

### createAuthorizationCode

Handle the creation of the authorization code.

```php
public createAuthorizationCode(mixed $client_id, mixed $user_id, string $redirect_uri, string $scope = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | - Client identifier related to the authorization code |
| `$user_id` | **mixed** | - User ID associated with the authorization code |
| `$redirect_uri` | **string** | - An absolute URI to which the authorization server will redirect the<br />user-agent to when the end-user authorization step is completed. |
| `$scope` | **string** | - OPTIONAL Scopes to be stored in space-separated string. |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4 - 

***


***
> Automatically generated on 2025-03-15
