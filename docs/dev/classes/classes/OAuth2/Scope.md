
# Scope





* Full name: `\OAuth2\Scope`
* This class implements:
[`\OAuth2\ScopeInterface`](./ScopeInterface.md)

**See Also:**

* \OAuth2\ScopeInterface - 



## Properties


### storage



```php
protected $storage
```






***

## Methods


### __construct

Constructor

```php
public __construct(mixed $storage = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **mixed** | - Either an array of supported scopes, or an instance of OAuth2\Storage\ScopeInterface |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



***

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

### scopeExists

Check if the provided scope exists in storage.

```php
public scopeExists(string $scope): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **string** | - A space-separated string of scopes. |


**Return Value:**

- TRUE if it exists, FALSE otherwise.




***

### getScopeFromRequest

Return scope info from request

```php
public getScopeFromRequest(\OAuth2\RequestInterface $request): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |





***

### getDefaultScope

The default scope to use in the event the client
does not request one. By returning "false", a
request_error is returned by the server to force a
scope request by the client. By returning "null",
opt out of requiring scopes

```php
public getDefaultScope(null $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **null** |  |





***

### getReservedScopes

Get reserved scopes needed by the server.

```php
public getReservedScopes(): array
```

In case OpenID Connect is used, these scopes must include:
'openid', offline_access'.







**Return Value:**

- An array of reserved scopes.




***


***
> Automatically generated on 2025-03-15
