
# Fbrowser

Base controller class for Modules.



* Full name: `\Zotlabs\Module\Fbrowser`
* Parent class: [`\Zotlabs\Web\Controller`](../Web/Controller.md)




## Methods


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

### folder1



```php
private static folder1(mixed $el): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$el` | **mixed** |  |





***

### files1



```php
private static files1(mixed $rr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rr` | **mixed** |  |





***

### files2



```php
private static files2(mixed $rr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rr` | **mixed** |  |





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
