
# Embedphotos

Base controller class for Modules.



* Full name: `\Zotlabs\Module\Embedphotos`
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

### post

Process POST requests.

```php
public post(): string
```









**Return Value:**

A JSON string.




***

### photolink



```php
protected static photolink(mixed $resource): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$resource` | **mixed** |  |





***

### embedphotos_widget_album



```php
protected embedphotos_widget_album(array $args): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** | associative array with<br />* \e array \b channel<br />* \e string \b album |


**Return Value:**

with HTML code from 'photo_album.tpl'




**See Also:**

*  - \\Zotlabs\\Widget\\Album::widget()

***

### embedphotos_album_list



```php
protected embedphotos_album_list(): null|array
```












**See Also:**

* \Zotlabs\Module\photos_albums_list() - 

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
