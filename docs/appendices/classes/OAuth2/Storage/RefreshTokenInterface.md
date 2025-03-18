
# RefreshTokenInterface

Implement this interface to specify where the OAuth2 Server
should get/save refresh tokens for the "Refresh Token"
grant type



* Full name: `\OAuth2\Storage\RefreshTokenInterface`



## Methods


### getRefreshToken

Grant refresh access tokens.

```php
public getRefreshToken(mixed $refresh_token): \OAuth2\Storage\An
```

Retrieve the stored data for the given refresh token.

Required for OAuth2::GRANT_TYPE_REFRESH_TOKEN.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **mixed** | <br />Refresh token to be check with. |


**Return Value:**

associative array as below, and NULL if the refresh_token is
invalid:
- refresh_token: Refresh token identifier.
- client_id: Client identifier.
- user_id: User identifier.
- expires: Expiration unix timestamp, or 0 if the token doesn't expire.
- scope: (optional) Scope values in space-separated string.




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-6 - 

***

### setRefreshToken

Take the provided refresh token values and store them somewhere.

```php
public setRefreshToken(mixed $refresh_token, mixed $client_id, mixed $user_id, mixed $expires, mixed $scope = null): mixed
```

This function should be the storage counterpart to getRefreshToken().

If storage fails for some reason, we're not currently checking for
any sort of success/failure, so you should bail out of the script
and provide a descriptive fail message.

Required for OAuth2::GRANT_TYPE_REFRESH_TOKEN.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **mixed** | <br />Refresh token to be stored. |
| `$client_id` | **mixed** | <br />Client identifier to be stored. |
| `$user_id` | **mixed** | <br />User identifier to be stored. |
| `$expires` | **mixed** | <br />Expiration timestamp to be stored. 0 if the token doesn&#039;t expire. |
| `$scope` | **mixed** | <br />(optional) Scopes to be stored in space-separated string. |





***

### unsetRefreshToken

Expire a used refresh token.

```php
public unsetRefreshToken(mixed $refresh_token): mixed
```

This is not explicitly required in the spec, but is almost implied.
After granting a new refresh token, the old one is no longer useful and
so should be forcibly expired in the data store so it can't be used again.

If storage fails for some reason, we're not currently checking for
any sort of success/failure, so you should bail out of the script
and provide a descriptive fail message.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **mixed** | <br />Refresh token to be expired. |





***


***
> Automatically generated on 2025-03-18
