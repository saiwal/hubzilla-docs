
# AuthorizationCodeInterface

Implement this interface to specify where the OAuth2 Server
should get/save authorization codes for the "Authorization Code"
grant type



* Full name: `\OAuth2\OpenID\Storage\AuthorizationCodeInterface`
* Parent interfaces: [`\OAuth2\Storage\AuthorizationCodeInterface`](../../Storage/AuthorizationCodeInterface.md)


## Methods


### setAuthorizationCode

Take the provided authorization code values and store them somewhere.

```php
public setAuthorizationCode(string $code, mixed $client_id, mixed $user_id, string $redirect_uri, int $expires, string $scope = null, string $id_token = null, mixed $code_challenge = null, mixed $code_challenge_method = null): mixed
```

This function should be the storage counterpart to getAuthCode().

If storage fails for some reason, we're not currently checking for
any sort of success/failure, so you should bail out of the script
and provide a descriptive fail message.

Required for OAuth2::GRANT_TYPE_AUTH_CODE.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | - authorization code to be stored. |
| `$client_id` | **mixed** | - client identifier to be stored. |
| `$user_id` | **mixed** | - user identifier to be stored. |
| `$redirect_uri` | **string** | - redirect URI(s) to be stored in a space-separated string. |
| `$expires` | **int** | - expiration to be stored as a Unix timestamp. |
| `$scope` | **string** | - OPTIONAL scopes to be stored in space-separated string. |
| `$id_token` | **string** | - OPTIONAL the OpenID Connect id_token. |
| `$code_challenge` | **mixed** |  |
| `$code_challenge_method` | **mixed** |  |





***


## Inherited methods


### getAuthorizationCode

Fetch authorization code data (probably the most common grant type).

```php
public getAuthorizationCode(mixed $code): \OAuth2\Storage\An
```

Retrieve the stored data for the given authorization code.

Required for OAuth2::GRANT_TYPE_AUTH_CODE.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **mixed** | <br />Authorization code to be check with. |


**Return Value:**

associative array as below, and NULL if the code is invalid




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4.1 - 

***

### setAuthorizationCode

Take the provided authorization code values and store them somewhere.

```php
public setAuthorizationCode(string $code, mixed $client_id, mixed $user_id, string $redirect_uri, int $expires, string $scope = null): mixed
```

This function should be the storage counterpart to getAuthCode().

If storage fails for some reason, we're not currently checking for
any sort of success/failure, so you should bail out of the script
and provide a descriptive fail message.

Required for OAuth2::GRANT_TYPE_AUTH_CODE.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | - Authorization code to be stored. |
| `$client_id` | **mixed** | - Client identifier to be stored. |
| `$user_id` | **mixed** | - User identifier to be stored. |
| `$redirect_uri` | **string** | - Redirect URI(s) to be stored in a space-separated string. |
| `$expires` | **int** | - Expiration to be stored as a Unix timestamp. |
| `$scope` | **string** | - OPTIONAL Scopes to be stored in space-separated string. |





***

### expireAuthorizationCode

once an Authorization Code is used, it must be expired

```php
public expireAuthorizationCode(mixed $code): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **mixed** |  |





**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4.1.2 - The client MUST NOT use the authorization code
more than once.  If an authorization code is used more than
once, the authorization server MUST deny the request and SHOULD
revoke (when possible) all tokens previously issued based on
that authorization code

***


***
> Automatically generated on 2025-03-18
