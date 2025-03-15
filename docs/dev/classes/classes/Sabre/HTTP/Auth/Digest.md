***

# Digest

HTTP Digest Authentication handler.

Use this class for easy http digest authentication.
Instructions:

 1. Create the object
 2. Call the setRealm() method with the realm you plan to use
 3. Call the init method function.
 4. Call the getUserName() function. This function may return null if no
    authentication information was supplied. Based on the username you
    should check your internal database for either the associated password,
    or the so-called A1 hash of the digest.
 5. Call either validatePassword() or validateA1(). This will return true
    or false.
 6. To make sure an authentication prompt is displayed, call the
    requireLogin() method.

* Full name: `\Sabre\HTTP\Auth\Digest`
* Parent class: [`\Sabre\HTTP\Auth\AbstractAuth`](./AbstractAuth.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`QOP_AUTH`|public| |1|
|`QOP_AUTHINT`|public| |2|

## Properties


### nonce



```php
protected $nonce
```






***

### opaque



```php
protected $opaque
```






***

### digestParts



```php
protected $digestParts
```






***

### A1



```php
protected $A1
```






***

### qop



```php
protected $qop
```






***

## Methods


### __construct

Initializes the object.

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

### init

Gathers all information from the headers.

```php
public init(): mixed
```

This method needs to be called prior to anything else.










***

### setQOP

Sets the quality of protection value.

```php
public setQOP(int $qop): mixed
```

Possible values are:
  Sabre\HTTP\DigestAuth::QOP_AUTH
  Sabre\HTTP\DigestAuth::QOP_AUTHINT

Multiple values can be specified using logical OR.

QOP_AUTHINT ensures integrity of the request body, but this is not
supported by most HTTP clients. QOP_AUTHINT also requires the entire
request body to be md5'ed, which can put strains on CPU and memory.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$qop` | **int** |  |





***

### validateA1

Validates the user.

```php
public validateA1(string $A1): bool
```

The A1 parameter should be md5($username . ':' . $realm . ':' . $password);






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$A1` | **string** |  |





***

### validatePassword

Validates authentication through a password. The actual password must be provided here.

```php
public validatePassword(string $password): bool
```

It is strongly recommended not store the password in plain-text and use validateA1 instead.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$password` | **string** |  |





***

### getUsername

Returns the username for the request.

```php
public getUsername(): string|null
```

Returns null if there were none.










***

### validate

Validates the digest challenge.

```php
protected validate(): bool
```












***

### requireLogin

Returns an HTTP 401 header, forcing login.

```php
public requireLogin(): mixed
```

This should be called when username and password are incorrect, or not supplied at all










***

### getDigest

This method returns the full digest string.

```php
public getDigest(): mixed
```

It should be compatible with mod_php format and other webservers.

If the header could not be found, null will be returned










***

### parseDigest

Parses the different pieces of the digest string into an array.

```php
protected parseDigest(string $digest): bool|array
```

This method returns false if an incomplete digest was supplied






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$digest` | **string** |  |





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
