
# Item

This is the POST destination for most all locally posted
text stuff. This function handles status, wall-to-wall status,
local comments, and remote coments that are posted on this site
(as opposed to being delivered in a feed).

Also processed here are posts and comments coming through the
statusnet/twitter API.
All of these become an "item" which is our basic unit of
information.
Posts that originate externally or do not fall into the above
posting categories go through item_store() instead of this function.

* Full name: `\Zotlabs\Module\Item`
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

### item_check_service_class



```php
public item_check_service_class(mixed $channel_id, mixed $iswebpage): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **mixed** |  |
| `$iswebpage` | **mixed** |  |





***

### extract_bb_poll_data



```php
public extract_bb_poll_data(mixed& $body, mixed $item): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$body` | **mixed** |  |
| `$item` | **mixed** |  |





***

### extract_poll_data



```php
public extract_poll_data(mixed $poll, mixed $item): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$poll` | **mixed** |  |
| `$item` | **mixed** |  |





***

### add_listeners



```php
public add_listeners(mixed $item): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### init_zot_request



```php
private init_zot_request(): mixed
```












***

### init_as_request



```php
private init_as_request(): mixed
```












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
> Automatically generated on 2025-03-18
