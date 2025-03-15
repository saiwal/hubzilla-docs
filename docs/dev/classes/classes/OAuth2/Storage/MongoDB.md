***

# MongoDB

Simple MongoDB storage for all storage types

NOTE: This class is meant to get users started
quickly. If your application requires further
customization, extend this class or create your own.

NOTE: Passwords are stored in plaintext, which is never
a good idea.  Be sure to override this for your application

* Full name: `\OAuth2\Storage\MongoDB`
* This class implements:
[`\OAuth2\Storage\AuthorizationCodeInterface`](./AuthorizationCodeInterface.md), [`\OAuth2\Storage\UserCredentialsInterface`](./UserCredentialsInterface.md), [`\OAuth2\Storage\AccessTokenInterface`](./AccessTokenInterface.md), [`\OAuth2\Storage\ClientCredentialsInterface`](./ClientCredentialsInterface.md), [`\OAuth2\Storage\RefreshTokenInterface`](./RefreshTokenInterface.md), [`\OAuth2\Storage\JwtBearerInterface`](./JwtBearerInterface.md), [`\OAuth2\Storage\PublicKeyInterface`](./PublicKeyInterface.md), [`\OAuth2\OpenID\Storage\AuthorizationCodeInterface`](../OpenID/Storage/AuthorizationCodeInterface.md)



## Properties


### db



```php
protected $db
```






***

### config



```php
protected $config
```






***

## Methods


### __construct



```php
public __construct(mixed $connection, mixed $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$connection` | **mixed** |  |
| `$config` | **mixed** |  |





***

### checkClientCredentials

Make sure that the client credentials is valid.

```php
public checkClientCredentials(mixed $client_id, mixed $client_secret = null): true
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be check with. |
| `$client_secret` | **mixed** | <br />(optional) If a secret is required, check that they&#039;ve given the right one. |


**Return Value:**

if the client credentials are valid, and MUST return FALSE if it isn't.




***

### isPublicClient

Determine if the client is a "public" client, and therefore
does not require passing credentials for certain grant types

```php
public isPublicClient(mixed $client_id): true
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be check with. |


**Return Value:**

if the client is public, and FALSE if it isn't.




***

### getClientDetails

Get client details corresponding client_id.

```php
public getClientDetails(mixed $client_id): array
```

OAuth says we should store request URIs for each registered client.
Implement this function to grab the stored URI for a given client id.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be check with. |


**Return Value:**


Client details. The only mandatory key in the array is "redirect_uri".
This function MUST return FALSE if the given client does not exist or is
invalid. "redirect_uri" can be space-delimited to allow for multiple valid uris.
<code>
return array(
"redirect_uri" => REDIRECT_URI,      // REQUIRED redirect_uri registered for the client
"client_id"    => CLIENT_ID,         // OPTIONAL the client id
"grant_types"  => GRANT_TYPES,       // OPTIONAL an array of restricted grant types
"user_id"      => USER_ID,           // OPTIONAL the user identifier associated with this client
"scope"        => SCOPE,             // OPTIONAL the scopes allowed for this client
);
</code>




***

### setClientDetails



```php
public setClientDetails(mixed $client_id, mixed $client_secret = null, mixed $redirect_uri = null, mixed $grant_types = null, mixed $scope = null, mixed $user_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$client_secret` | **mixed** |  |
| `$redirect_uri` | **mixed** |  |
| `$grant_types` | **mixed** |  |
| `$scope` | **mixed** |  |
| `$user_id` | **mixed** |  |





***

### checkRestrictedGrantType

Check restricted grant types of corresponding client identifier.

```php
public checkRestrictedGrantType(mixed $client_id, mixed $grant_type): true
```

If you want to restrict clients to certain grant types, override this
function.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be check with. |
| `$grant_type` | **mixed** | <br />Grant type to be check with |


**Return Value:**

if the grant type is supported by this client identifier, and
FALSE if it isn't.




***

### getAccessToken

Look up the supplied oauth_token from storage.

```php
public getAccessToken(mixed $access_token): array|null
```

We need to retrieve access token data as we create and verify tokens.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **mixed** |  |


**Return Value:**

- An associative array as below, and return NULL if the supplied oauth_token is invalid:




***

### setAccessToken

Store the supplied access token values to storage.

```php
public setAccessToken(mixed $access_token, mixed $client_id, mixed $user_id, mixed $expires, mixed $scope = null): mixed
```

We need to store access token data as we create and verify tokens.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **mixed** |  |
| `$client_id` | **mixed** | - client identifier to be stored. |
| `$user_id` | **mixed** | - user identifier to be stored. |
| `$expires` | **mixed** | - expiration to be stored as a Unix timestamp. |
| `$scope` | **mixed** | - OPTIONAL Scopes to be stored in space-separated string. |





***

### unsetAccessToken



```php
public unsetAccessToken(mixed $access_token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token` | **mixed** |  |





***

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




***

### setAuthorizationCode

Take the provided authorization code values and store them somewhere.

```php
public setAuthorizationCode(mixed $code, mixed $client_id, mixed $user_id, mixed $redirect_uri, mixed $expires, mixed $scope = null, mixed $id_token = null, mixed $code_challenge = null, mixed $code_challenge_method = null): mixed
```

This function should be the storage counterpart to getAuthCode().

If storage fails for some reason, we're not currently checking for
any sort of success/failure, so you should bail out of the script
and provide a descriptive fail message.

Required for OAuth2::GRANT_TYPE_AUTH_CODE.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **mixed** | - Authorization code to be stored. |
| `$client_id` | **mixed** | - Client identifier to be stored. |
| `$user_id` | **mixed** | - User identifier to be stored. |
| `$redirect_uri` | **mixed** | - Redirect URI(s) to be stored in a space-separated string. |
| `$expires` | **mixed** | - Expiration to be stored as a Unix timestamp. |
| `$scope` | **mixed** | - OPTIONAL Scopes to be stored in space-separated string. |
| `$id_token` | **mixed** |  |
| `$code_challenge` | **mixed** |  |
| `$code_challenge_method` | **mixed** |  |





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





***

### checkUserCredentials

Grant access tokens for basic user credentials.

```php
public checkUserCredentials(mixed $username, mixed $password): true
```

Check the supplied username and password for validity.

You can also use the $client_id param to do any checks required based
on a client, if you need that.

Required for OAuth2::GRANT_TYPE_USER_CREDENTIALS.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **mixed** | <br />Username to be check with. |
| `$password` | **mixed** | <br />Password to be check with. |


**Return Value:**

if the username and password are valid, and FALSE if it isn't.
Moreover, if the username and password are valid, and you want to




***

### getUserDetails



```php
public getUserDetails(mixed $username): array|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **mixed** | - username to get details for |


**Return Value:**

- the associated "user_id" and optional "scope" values
This function MUST return FALSE if the requested user does not exist or is
invalid. "scope" is a space-separated list of restricted scopes.




***

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

### checkPassword



```php
protected checkPassword(mixed $user, mixed $password): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$user` | **mixed** |  |
| `$password` | **mixed** |  |





***

### getUser



```php
public getUser(mixed $username): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **mixed** |  |





***

### setUser



```php
public setUser(mixed $username, mixed $password, mixed $firstName = null, mixed $lastName = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **mixed** |  |
| `$password` | **mixed** |  |
| `$firstName` | **mixed** |  |
| `$lastName` | **mixed** |  |





***

### getClientKey

Get the public key associated with a client_id

```php
public getClientKey(mixed $client_id, mixed $subject): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be checked with. |
| `$subject` | **mixed** |  |


**Return Value:**

Return the public key for the client_id if it exists, and MUST return FALSE if it doesn't.




***

### getClientScope

Get the scope associated with this client

```php
public getClientScope(mixed $client_id): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |


**Return Value:**

the space-delineated scope list for the specified client_id




***

### getJti

Get a jti (JSON token identifier) by matching against the client_id, subject, audience and expiration.

```php
public getJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expires, mixed $jti): \OAuth2\Storage\An
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to match. |
| `$subject` | **mixed** | <br />The subject to match. |
| `$audience` | **mixed** | <br />The audience to match. |
| `$expires` | **mixed** |  |
| `$jti` | **mixed** | <br />The jti to match. |


**Return Value:**

associative array as below, and return NULL if the jti does not exist.
- issuer: Stored client identifier.
- subject: Stored subject.
- audience: Stored audience.
- expires: Stored expiration in unix timestamp.
- jti: The stored jti.




***

### setJti

Store a used jti so that we can check against it to prevent replay attacks.

```php
public setJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expires, mixed $jti): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to insert. |
| `$subject` | **mixed** | <br />The subject to insert. |
| `$audience` | **mixed** | <br />The audience to insert. |
| `$expires` | **mixed** |  |
| `$jti` | **mixed** | <br />The jti to insert. |





***

### getPublicKey



```php
public getPublicKey(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getPrivateKey



```php
public getPrivateKey(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getEncryptionAlgorithm



```php
public getEncryptionAlgorithm(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### collection



```php
protected collection(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
