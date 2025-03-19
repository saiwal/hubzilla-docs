
# Help

You can create local site resources in doc/Site.md and either link to doc/Home.md for the standard resources
or use our include mechanism to include it on your local page.



* Full name: `\Zotlabs\Module\Help`
* Parent class: [`\Zotlabs\Web\Controller`](../Web/Controller.md)



## Properties


### heading_slug



```php
private string $heading_slug
```






***

## Methods


### init

Pre-check before processing request.

```php
public init(): mixed
```

Determine language requested, and ensure that a topic was requested.
If no topic was requested, redirect to the about page, and abort
processing.










***

### get

Process get request for the help module.

```php
public get(): string
```

Loads the correct help file from the `doc/` directory, and passes it to
the help template in `view/tpl/help.tpl`.

If the requested help topic does not exist for the currently selected
language, a 404 status is returned instead.

This function currently also handles search and serving static assets
that may be used by the help files.







**Return Value:**

The rendered help page or a 404 page if help topic was
not found.




***

### render_content



```php
public render_content(): string
```












***

### render_help_file



```php
public render_help_file(string $file_name, string $file_type): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **string** |  |
| `$file_type` | **string** |  |





***

### get_page_title



```php
public get_page_title(): string
```












***

### get_toc_heading



```php
public get_toc_heading(): string
```












***

### get_heading



```php
private get_heading(): string
```












***

### set_page_title

Set the page title to an unslugified version of the file name.

```php
private set_page_title(): void
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

### determine_help_language

Determines help language.

```php
private determine_help_language(): mixed
```

If the language was specified in the URL, override the language preference
of the browser. Default to English if both of these are absent.

Updates the `$lang` property of the module.










***

### find_help_file

Find the full path name of the file, given it's base path and
the language of the request.

```php
private find_help_file(string $base_path, string $lang): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base_path` | **string** | The path of the file to find, relative to the<br />doc root path, and without the extension. |
| `$lang` | **string** |  |





***

### missing_translation



```php
public missing_translation(): bool
```












***

### missing_translation_message



```php
public missing_translation_message(): string
```












***


***
> Automatically generated on 2025-03-19
