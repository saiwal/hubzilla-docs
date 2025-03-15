
# ScopeInterface

Class to handle scope implementation logic



* Full name: `\OAuth2\ScopeInterface`
* Parent interfaces: [`\OAuth2\Storage\ScopeInterface`](./Storage/ScopeInterface.md)
**See Also:**

* \OAuth2\Storage\ScopeInterface - 



## Methods


### checkScope

Check if everything in required scope is contained in available scope.

```php
public checkScope(string $required_scope, string $available_scope): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$required_scope` | **string** | - A space-separated string of scopes. |
| `$available_scope` | **string** | - A space-separated string of scopes. |


**Return Value:**

- TRUE if everything in required scope is contained in available scope and FALSE
if it isn't.




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-7 - 

***

### getScopeFromRequest

Return scope info from request

```php
public getScopeFromRequest(\OAuth2\RequestInterface $request): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** | - Request object to check |


**Return Value:**

- representation of requested scope




***


## Inherited methods


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
> Automatically generated on 2025-03-15
