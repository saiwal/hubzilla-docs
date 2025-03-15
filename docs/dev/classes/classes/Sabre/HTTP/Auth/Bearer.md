***

# Bearer

HTTP Bearer authentication utility.

This class helps you setup bearer auth. The process is fairly simple:

1. Instantiate the class.
2. Call getToken (this will return null or a token as string)
3. If you didn't get a valid token, call 'requireLogin'

* Full name: `\Sabre\HTTP\Auth\Bearer`
* Parent class: [`\Sabre\HTTP\Auth\AbstractAuth`](./AbstractAuth.md)




## Methods


### getToken

This method returns a string with an access token.

```php
public getToken(): string|null
```

If no token was found, this method returns null.










***

### requireLogin

This method sends the needed HTTP header and status code (401) to force
authentication.

```php
public requireLogin(): mixed
```












***


## Inherited methods


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
