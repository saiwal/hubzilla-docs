
# ResponseInterface

Interface which represents an object response.  Meant to handle and display the proper OAuth2 Responses
for errors and successes



* Full name: `\OAuth2\ResponseInterface`

**See Also:**

* \OAuth2\Response - 



## Methods


### addParameters



```php
public addParameters(array $parameters): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameters` | **array** |  |





***

### addHttpHeaders



```php
public addHttpHeaders(array $httpHeaders): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$httpHeaders` | **array** |  |





***

### setStatusCode



```php
public setStatusCode(int $statusCode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$statusCode` | **int** |  |





***

### setError



```php
public setError(int $statusCode, string $name, string $description = null, string $uri = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$statusCode` | **int** |  |
| `$name` | **string** |  |
| `$description` | **string** |  |
| `$uri` | **string** |  |





***

### setRedirect



```php
public setRedirect(int $statusCode, string $url, string $state = null, string $error = null, string $errorDescription = null, string $errorUri = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$statusCode` | **int** |  |
| `$url` | **string** |  |
| `$state` | **string** |  |
| `$error` | **string** |  |
| `$errorDescription` | **string** |  |
| `$errorUri` | **string** |  |





***

### getParameter



```php
public getParameter(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***


***
> Automatically generated on 2025-03-15
