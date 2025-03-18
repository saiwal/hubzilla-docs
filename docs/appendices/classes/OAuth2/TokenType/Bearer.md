
# Bearer





* Full name: `\OAuth2\TokenType\Bearer`
* This class implements:
[`\OAuth2\TokenType\TokenTypeInterface`](./TokenTypeInterface.md)



## Properties


### config



```php
private $config
```






***

## Methods


### __construct



```php
public __construct(array $config = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **array** |  |





***

### getTokenType

Token type identification string

```php
public getTokenType(): mixed
```

ex: "bearer" or "mac"










***

### requestHasToken

Check if the request has supplied token

```php
public requestHasToken(\OAuth2\RequestInterface $request): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |





**See Also:**

* https://github.com/bshaffer/oauth2-server-php/issues/349#issuecomment-37993588 - 

***

### getAccessTokenParameter

This is a convenience function that can be used to get the token, which can then
be passed to getAccessTokenData(). The constraints specified by the draft are
attempted to be adheared to in this method.

```php
public getAccessTokenParameter(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```

As per the Bearer spec (draft 8, section 2) - there are three ways for a client
to specify the bearer token, in order of preference: Authorization Header,
POST and GET.

NB: Resource servers MUST accept tokens via the Authorization scheme
(http://tools.ietf.org/html/rfc6750#section-2).






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





**See Also:**

* http://tools.ietf.org/html/rfc6750#section-2.1 - * http://tools.ietf.org/html/rfc6750#section-2.2 - * http://tools.ietf.org/html/rfc6750#section-2.3 - Old Android version bug (at least with version 2.2)* http://code.google.com/p/android/issues/detail?id=6684 - 

***


***
> Automatically generated on 2025-03-18
