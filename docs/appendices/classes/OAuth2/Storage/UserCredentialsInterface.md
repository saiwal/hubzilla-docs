
# UserCredentialsInterface

Implement this interface to specify where the OAuth2 Server
should retrieve user credentials for the
"Resource Owner Password Credentials" grant type



* Full name: `\OAuth2\Storage\UserCredentialsInterface`



## Methods


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




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-4.3 - 

***

### getUserDetails



```php
public getUserDetails(string $username): array|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** | - username to get details for |


**Return Value:**

- the associated "user_id" and optional "scope" values
This function MUST return FALSE if the requested user does not exist or is
invalid. "scope" is a space-separated list of restricted scopes.




***


***
> Automatically generated on 2025-03-18
