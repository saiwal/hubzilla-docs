
# Sse_bs

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

* Full name: `\Zotlabs\Module\Sse_bs`
* Parent class: [`\Zotlabs\Web\Controller`](../Web/Controller.md)



## Properties


### uid



```php
public static $uid
```



* This property is **static**.


***

### ob_hash



```php
public static $ob_hash
```



* This property is **static**.


***

### sse_id



```php
public static $sse_id
```



* This property is **static**.


***

### vnotify



```php
public static $vnotify
```



* This property is **static**.


***

### evdays



```php
public static $evdays
```



* This property is **static**.


***

### limit



```php
public static $limit
```



* This property is **static**.


***

### offset



```php
public static $offset
```



* This property is **static**.


***

### xchans



```php
public static $xchans
```



* This property is **static**.


***

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

### mark_read



```php
public mark_read(mixed $arr): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |





***

### bs_network



```php
public bs_network(mixed $notifications): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$notifications` | **mixed** |  |





***

### bs_dm



```php
public bs_dm(mixed $notifications): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$notifications` | **mixed** |  |





***

### bs_home



```php
public bs_home(mixed $notifications): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$notifications` | **mixed** |  |





***

### bs_pubs



```php
public bs_pubs(mixed $notifications): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$notifications` | **mixed** |  |





***

### bs_notify



```php
public bs_notify(): mixed
```












***

### bs_intros



```php
public bs_intros(): mixed
```












***

### bs_forums



```php
public bs_forums(): mixed
```












***

### bs_files



```php
public bs_files(): mixed
```












***

### bs_all_events



```php
public bs_all_events(): mixed
```












***

### bs_register



```php
public bs_register(): mixed
```












***

### bs_info_notice



```php
public bs_info_notice(): mixed
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
