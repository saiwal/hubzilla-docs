
# TestRequest

OAuth2\Request
This class is taken from the Symfony2 Framework and is part of the Symfony package.



* Full name: `\OAuth2\Request\TestRequest`
* Parent class: [`\OAuth2\Request`](../Request.md)
* This class implements:
[`\OAuth2\RequestInterface`](../RequestInterface.md)



## Properties


### query



```php
public $query
```






***

### request



```php
public $request
```






***

### server



```php
public $server
```






***

### headers



```php
public $headers
```






***

## Methods


### __construct

Constructor.

```php
public __construct(): mixed
```












***

### query



```php
public query(mixed $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$default` | **mixed** |  |





***

### request



```php
public request(mixed $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$default` | **mixed** |  |





***

### server



```php
public server(mixed $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$default` | **mixed** |  |





***

### getAllQueryParameters



```php
public getAllQueryParameters(): array
```












***

### setQuery



```php
public setQuery(array $query): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$query` | **array** |  |





***

### setMethod



```php
public setMethod(mixed $method): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **mixed** |  |





***

### setPost



```php
public setPost(array $params): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** |  |





***

### createPost



```php
public static createPost(array $params = array()): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** |  |





***


## Inherited methods


### __construct

Constructor.

```php
public __construct(array $query = array(), array $request = array(), array $attributes = array(), array $cookies = array(), array $files = array(), array $server = array(), string $content = null, array $headers = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$query` | **array** | - The GET parameters |
| `$request` | **array** | - The POST parameters |
| `$attributes` | **array** | - The request attributes (parameters parsed from the PATH_INFO, ...) |
| `$cookies` | **array** | - The COOKIE parameters |
| `$files` | **array** | - The FILES parameters |
| `$server` | **array** | - The SERVER parameters |
| `$content` | **string** | - The raw body data |
| `$headers` | **array** | - The headers |





***

### initialize

Sets the parameters for this request.

```php
public initialize(array $query = array(), array $request = array(), array $attributes = array(), array $cookies = array(), array $files = array(), array $server = array(), string $content = null, array $headers = null): mixed
```

This method also re-initializes all properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$query` | **array** | - The GET parameters |
| `$request` | **array** | - The POST parameters |
| `$attributes` | **array** | - The request attributes (parameters parsed from the PATH_INFO, ...) |
| `$cookies` | **array** | - The COOKIE parameters |
| `$files` | **array** | - The FILES parameters |
| `$server` | **array** | - The SERVER parameters |
| `$content` | **string** | - The raw body data |
| `$headers` | **array** | - The headers |





***

### query



```php
public query(string $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$default` | **mixed** |  |





***

### request



```php
public request(string $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$default` | **mixed** |  |





***

### server



```php
public server(string $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$default` | **mixed** |  |





***

### headers



```php
public headers(string $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$default` | **mixed** |  |





***

### getAllQueryParameters



```php
public getAllQueryParameters(): array
```












***

### getContent

Returns the request body content.

```php
public getContent(bool $asResource = false): string|resource
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$asResource` | **bool** | - If true, a resource will be returned |


**Return Value:**

- The request body content or a resource to read the body stream.



**Throws:**

- [`LogicException`](../../LogicException.md)



***

### getHeadersFromServer



```php
private getHeadersFromServer(array $server): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **array** |  |





***

### createFromGlobals

Creates a new request with values from PHP's super globals.

```php
public static createFromGlobals(): \OAuth2\Request
```



* This method is **static**.





**Return Value:**

- A new request




***


***
> Automatically generated on 2025-03-15
