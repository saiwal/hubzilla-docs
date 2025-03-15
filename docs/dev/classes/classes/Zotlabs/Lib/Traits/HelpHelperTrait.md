***

# HelpHelperTrait





* Full name: `\Zotlabs\Lib\Traits\HelpHelperTrait`



## Properties


### file_name



```php
private string $file_name
```






***

### file_type



```php
private string $file_type
```






***

### lang

Associative array containing the detected language.

```php
private array $lang
```






***

## Methods


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
> Automatically generated on 2025-03-15

