***

# HttpBasic

Validate a client via Http Basic authentication



* Full name: `\OAuth2\ClientAssertionType\HttpBasic`
* This class implements:
[`\OAuth2\ClientAssertionType\ClientAssertionTypeInterface`](./ClientAssertionTypeInterface.md)



## Properties


### clientData



```php
private $clientData
```






***

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

Config array $config should look as follows:

```php
public __construct(\OAuth2\Storage\ClientCredentialsInterface $storage, array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$storage` | **\OAuth2\Storage\ClientCredentialsInterface** | Storage |
| `$config` | **array** | Configuration options for the server |





***

### validateRequest

Validate the OAuth request

```php
public validateRequest(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |




**Throws:**

- [`LogicException`](../../LogicException.md)



***

### getClientId

Get the client id

```php
public getClientId(): mixed
```












***

### getClientCredentials

Internal function used to get the client credentials from HTTP basic
auth or POST data.

```php
public getClientCredentials(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response = null): array|null
```

According to the spec (draft 20), the client_id can be provided in
the Basic Authorization header (recommended) or via GET/POST.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |


**Return Value:**

A list containing the client identifier and password, for example:




**See Also:**

* http://tools.ietf.org/html/rfc6749#section-2.3.1 - 

***


***
> Automatically generated on 2025-03-15
