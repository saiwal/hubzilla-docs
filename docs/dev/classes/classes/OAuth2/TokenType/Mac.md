
# Mac

This is not yet supported!



* Full name: `\OAuth2\TokenType\Mac`
* This class implements:
[`\OAuth2\TokenType\TokenTypeInterface`](./TokenTypeInterface.md)




## Methods


### getTokenType

Token type identification string

```php
public getTokenType(): mixed
```

ex: "bearer" or "mac"










***

### getAccessTokenParameter

Retrieves the token string from the request object

```php
public getAccessTokenParameter(\OAuth2\RequestInterface $request, \OAuth2\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth2\RequestInterface** |  |
| `$response` | **\OAuth2\ResponseInterface** |  |





***


***
> Automatically generated on 2025-03-15
