***

# AbstractAuth

HTTP Authentication base class.

This class provides some common functionality for the various base classes.

* Full name: `\Sabre\HTTP\Auth\AbstractAuth`
* This class is an **Abstract class**



## Properties


### realm

Authentication realm.

```php
protected string $realm
```






***

### request

Request object.

```php
protected \Sabre\HTTP\RequestInterface $request
```






***

### response

Response object.

```php
protected \Sabre\HTTP\ResponseInterface $response
```






***

## Methods


### __construct

Creates the object.

```php
public __construct(string $realm, \Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **string** |  |
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### requireLogin

This method sends the needed HTTP header and status code (401) to force
the user to login.

```php
public requireLogin(): mixed
```




* This method is **abstract**.







***

### getRealm

Returns the HTTP realm.

```php
public getRealm(): string
```












***


***
> Automatically generated on 2025-03-15
