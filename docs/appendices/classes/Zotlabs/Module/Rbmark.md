
# Rbmark

remote bookmark

https://yoursite/rbmark?f=&title=&url=&private=&remote_return=

This can be called via either GET or POST, use POST for long body content as suhosin often limits GET parameter length

f= placeholder, often required
title= link text
url= URL to bookmark
ischat=1 if this bookmark is a chatroom
private= Don't share this link
remote_return= absolute URL to return after posting is finished

* Full name: `\Zotlabs\Module\Rbmark`
* Parent class: [`\Zotlabs\Web\Controller`](../Web/Controller.md)




## Methods


### post

Process POST requests.

```php
public post(): void
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

### get_bookmark_folders



```php
private get_bookmark_folders(int $channel_id): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **int** |  |





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
