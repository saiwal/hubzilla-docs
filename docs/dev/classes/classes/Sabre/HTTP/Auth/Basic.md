
# Basic

HTTP Basic authentication utility.

This class helps you setup basic auth. The process is fairly simple:

1. Instantiate the class.
2. Call getCredentials (this will return null or a user/pass pair)
3. If you didn't get valid credentials, call 'requireLogin'

* Full name: `\Sabre\HTTP\Auth\Basic`
* Parent class: [`\Sabre\HTTP\Auth\AbstractAuth`](./AbstractAuth.md)




## Methods


### getCredentials

This method returns a numeric array with a username and password as the
only elements.

```php
public getCredentials(): array|null
```

If no credentials were found, this method returns null.










***

### requireLogin

This method sends the needed HTTP header and status code (401) to force
the user to login.

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
