
# AccessTokenInterface

Implement this interface to specify where the OAuth2 Server
should get/save access tokens



* Full name: `\OAuth2\Storage\AccessTokenInterface`



## Methods


### getAccessToken

Look up the supplied oauth_token from storage.

```php
public getAccessToken(string $oauth_token): array|null
```

We need to retrieve access token data as we create and verify tokens.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oauth_token` | **string** | - oauth_token to be check with. |


**Return Value:**

- An associative array as below, and return NULL if the supplied oauth_token is invalid:




***

### setAccessToken

Store the supplied access token values to storage.

```php
public setAccessToken(string $oauth_token, mixed $client_id, mixed $user_id, int $expires, string $scope = null): mixed
```

We need to store access token data as we create and verify tokens.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oauth_token` | **string** | - oauth_token to be stored. |
| `$client_id` | **mixed** | - client identifier to be stored. |
| `$user_id` | **mixed** | - user identifier to be stored. |
| `$expires` | **int** | - expiration to be stored as a Unix timestamp. |
| `$scope` | **string** | - OPTIONAL Scopes to be stored in space-separated string. |





***


***
> Automatically generated on 2025-03-18
