
# OAuth2TestVehicle

The OAuth2TestVehicle class is a way to test the registration of an OAuth2
client app. It allows you to walk through the steps of registering a client,
requesting an authorization code for that client, and then requesting an
access token for use in authentication against the Hubzilla API endpoints.



* Full name: `\Zotlabs\Module\OAuth2TestVehicle`
* Parent class: [`\Zotlabs\Web\Controller`](../Web/Controller.md)




## Methods


### init

Initialize request processing.

```php
public init(): mixed
```

This method is called before any other request processing, and
regardless of the request method. The theme is not yet loaded when
this method is invoked.










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
> Automatically generated on 2025-03-15
