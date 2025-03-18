
# AccessTokenInterface





* Full name: `\OAuth2\ResponseType\AccessTokenInterface`
* Parent interfaces: [`\OAuth2\ResponseType\ResponseTypeInterface`](./ResponseTypeInterface.md)


## Methods


### createAccessToken

Handle the creation of access token, also issue refresh token if supported / desirable.

```php
public createAccessToken(mixed $client_id, mixed $user_id, string $scope = null, bool $includeRefreshToken = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | - client identifier related to the access token. |
| `$user_id` | **mixed** | - user ID associated with the access token |
| `$scope` | **string** | - OPTONAL scopes to be stored in space-separated string. |
| `$includeRefreshToken` | **bool** | - if true, a new refresh_token will be added to the response |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-5 - 

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


***
> Automatically generated on 2025-03-18
