
# Owa

OpenWebAuth verifier and token generator
See spec/OpenWebAuth/Home.md
Requests to this endpoint should be signed using HTTP Signatures
using the 'Authorization: Signature' authentication method
If the signature verifies a token is returned.

This token may be exchanged for an authenticated cookie.

* Full name: `\Zotlabs\Module\Owa`
* Parent class: [`\Zotlabs\Web\Controller`](../Web/Controller.md)




## Methods


### init

Initialize request processing.

```php
public init(): void
```

This method is called before any other request processing, and
regardless of the request method. The theme is not yet loaded when
this method is invoked.










***

### validateAuthorizationHeader



```php
private validateAuthorizationHeader(): bool
```












***

### error

Terminates the request, and return a json error response.

```php
private error(string $msg): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **string** | The error message for the response. |





***


## Inherited methods


### init

Initialize request processing.

```php
public init(): mixed
```

This method is called before any other request processing, and
regardless of the request method. The theme is not yet loaded when
this method is invoked.










***

### post

Process POST requests.

```php
public post(): mixed
```

This method is called if the incoming request is a POST request. It is
invoked after the theme has been loaded. This method should not normally
render HTML output, as processing will fall through to the GET processing
if this method completes without error or stopping processing in other
ways.










***

### get

Process GET requests or the body part of POST requests.

```php
public get(): string
```

This method is called directly for GET requests, and immediately after the
`post()` method for POST requests.

It will return the module content as a HTML string.







**Return Value:**

HTML content for the module.




***


***
> Automatically generated on 2025-03-19
