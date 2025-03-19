
# Oep

Base controller class for Modules.

Modules should extend this class, and override the methods needed. Emtpy
default implementations allow Modules to only override the methods they
need.

The methods defined by this class is invoked in order:

  - init()
  - post() -- only for POST requests
  - get()

Modules which emit other serialisations besides HTML (XML,JSON, etc.) should
do so within the module `init` and/or `post` functions and then invoke
`killme()` to terminate further processing.

* Full name: `\Zotlabs\Module\Oep`
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

### oep_display_reply



```php
public oep_display_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### oep_cards_reply



```php
public oep_cards_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### oep_articles_reply



```php
public oep_articles_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### oep_mid_reply



```php
public oep_mid_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### oep_profile_reply



```php
public oep_profile_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### oep_album_reply



```php
public oep_album_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### oep_phototop_reply



```php
public oep_phototop_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### oep_photo_reply



```php
public oep_photo_reply(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





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
