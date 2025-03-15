***

# AuthorizationCode





* Full name: `\OAuth2\ResponseType\AuthorizationCode`
* This class implements:
[`\OAuth2\ResponseType\AuthorizationCodeInterface`](./AuthorizationCodeInterface.md)



## Properties


### storage



```php
protected $storage
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
