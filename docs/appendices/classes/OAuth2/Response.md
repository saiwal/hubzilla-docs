
# Response

Class to handle OAuth2 Responses in a graceful way.  Use this interface
to output the proper OAuth2 responses.



* Full name: `\OAuth2\Response`
* This class implements:
[`\OAuth2\ResponseInterface`](./ResponseInterface.md)

**See Also:**

* \OAuth2\OAuth2\ResponseInterface - This class borrows heavily from the Symfony2 Framework and is part of the symfony package
* \OAuth2\Symfony\Component\HttpFoundation\Request - (https://github.com/symfony/symfony)



## Properties


### version



```php
public string $version
```






***

### statusCode



```php
protected int $statusCode
```






***

### statusText



```php
protected string $statusText
```






***

### parameters



```php
protected array $parameters
```






***

### httpHeaders



```php
protected array $httpHeaders
```






***

### statusTexts



```php
public static array $statusTexts
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(array $parameters = array(), int $statusCode = 200, array $headers = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameters` | **array** |  |
| `$statusCode` | **int** |  |
| `$headers` | **array** |  |





***

### __toString

Converts the response object to string containing all headers and the response content.

```php
public __toString(): string
```









**Return Value:**

The response with headers and content




***

### buildHeader

Returns the build header line.

```php
protected buildHeader(string $name, string $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | The header name |
| `$value` | **string** | The header value |


**Return Value:**

The built header line




***

### getStatusCode



```php
public getStatusCode(): int
```












***

### setStatusCode



```php
public setStatusCode(int $statusCode, string $text = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$statusCode` | **int** |  |
| `$text` | **string** |  |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



***

### getStatusText



```php
public getStatusText(): string
```












***

### getParameters



```php
public getParameters(): array
```












***

### setParameters



```php
public setParameters(array $parameters): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameters` | **array** |  |





***

### addParameters



```php
public addParameters(array $parameters): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameters` | **array** |  |





***

### getParameter



```php
public getParameter(string $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$default` | **mixed** |  |





***

### setParameter



```php
public setParameter(string $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### setHttpHeaders



```php
public setHttpHeaders(array $httpHeaders): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$httpHeaders` | **array** |  |





***

### setHttpHeader



```php
public setHttpHeader(string $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





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

### getHttpHeaders



```php
public getHttpHeaders(): array
```












***

### getHttpHeader



```php
public getHttpHeader(string $name, mixed $default = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$default` | **mixed** |  |





***

### getResponseBody



```php
public getResponseBody(string $format = &#039;json&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **string** |  |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



***

### send



```php
public send(string $format = &#039;json&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **string** |  |





***

### setError



```php
public setError(int $statusCode, string $error, string $errorDescription = null, string $errorUri = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$statusCode` | **int** |  |
| `$error` | **string** |  |
| `$errorDescription` | **string** |  |
| `$errorUri` | **string** |  |




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



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




**Throws:**

- [`InvalidArgumentException`](../InvalidArgumentException.md)



***

### isInvalid



```php
public isInvalid(): bool
```












**See Also:**

* http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html - 

***

### isInformational



```php
public isInformational(): bool
```












***

### isSuccessful



```php
public isSuccessful(): bool
```












***

### isRedirection



```php
public isRedirection(): bool
```












***

### isClientError



```php
public isClientError(): bool
```












***

### isServerError



```php
public isServerError(): bool
```












***

### getHttpHeadersAsString

Function from Symfony2 HttpFoundation - output pretty header

```php
private getHttpHeadersAsString(array $headers): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **array** |  |





***

### beautifyHeaderName

Function from Symfony2 HttpFoundation - output pretty header

```php
private beautifyHeaderName(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### beautifyCallback

Function from Symfony2 HttpFoundation - output pretty header

```php
private beautifyCallback(array $match): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$match` | **array** |  |





***


***
> Automatically generated on 2025-03-18
