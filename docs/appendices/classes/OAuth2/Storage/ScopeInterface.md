
# ScopeInterface

Implement this interface to specify where the OAuth2 Server
should retrieve data involving the relevent scopes associated
with this implementation.



* Full name: `\OAuth2\Storage\ScopeInterface`



## Methods


### scopeExists

Check if the provided scope exists.

```php
public scopeExists(mixed $scope): true
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **mixed** | <br />A space-separated string of scopes. |


**Return Value:**

if it exists, FALSE otherwise.




***

### getDefaultScope

The default scope to use in the event the client
does not request one. By returning "false", a
request_error is returned by the server to force a
scope request by the client. By returning "null",
opt out of requiring scopes

```php
public getDefaultScope(mixed $client_id = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />An optional client id that can be used to return customized default scopes. |


**Return Value:**

representation of default scope, null if
scopes are not defined, or false to force scope
request by the client

ex:
    'default'
ex:
    null




***


***
> Automatically generated on 2025-03-18
