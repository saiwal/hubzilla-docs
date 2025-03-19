
# OAuth2Storage





* Full name: `\Zotlabs\Identity\OAuth2Storage`
* Parent class: [`Pdo`](../../OAuth2/Storage/Pdo.md)




## Methods


### checkUserCredentials



```php
public checkUserCredentials(string $username, string $password): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |





***

### getUserDetails



```php
public getUserDetails(string $username): array|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |





***

### checkPassword



```php
protected checkPassword(array $user, string $password): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$user` | **array** |  |
| `$password` | **string** |  |





***

### getUser



```php
public getUser(string $username): array|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |





***

### scopeExists



```php
public scopeExists(mixed $scope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **mixed** |  |





***

### getDefaultScope



```php
public getDefaultScope(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getUserClaims



```php
public getUserClaims(mixed $user_id, mixed $claims): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$user_id` | **mixed** |  |
| `$claims` | **mixed** |  |





***

### setUser

plaintext passwords are bad!  Override this for your application

```php
public setUser(string $username, string $password, string $firstName = null, string $lastName = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |
| `$firstName` | **string** |  |
| `$lastName` | **string** |  |





***


***
> Automatically generated on 2025-03-19
