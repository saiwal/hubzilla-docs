
# HTMLPurifier_LanguageFactory

Class responsible for generating HTMLPurifier_Language objects, managing
caching and fallbacks.



* Full name: `\HTMLPurifier_LanguageFactory`



## Properties


### cache

Cache of language code information used to load HTMLPurifier_Language objects.

```php
public $cache
```

Structure is: $factory->cache[$language_code][$key] = $value




***

### keys

Valid keys in the HTMLPurifier_Language object. Designates which
variables to slurp out of a message file.

```php
public $keys
```






***

### validator

Instance to validate language codes.

```php
protected $validator
```






***

### dir

Cached copy of dirname(__FILE__), directory of current file without
trailing slash.

```php
protected $dir
```






***

### mergeable_keys_map

Keys whose contents are a hash map and can be merged.

```php
protected $mergeable_keys_map
```






***

### mergeable_keys_list

Keys whose contents are a list and can be merged.

```php
protected $mergeable_keys_list
```






***

## Methods


### instance

Retrieve sole instance of the factory.

```php
public static instance(\HTMLPurifier_LanguageFactory $prototype = null): \HTMLPurifier_LanguageFactory
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **\HTMLPurifier_LanguageFactory** | Optional prototype to overload sole instance with,<br />or bool true to reset to default factory. |





***

### setup

Sets up the singleton, much like a constructor

```php
public setup(): mixed
```












***

### create

Creates a language object, handles class fallbacks

```php
public create(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context, bool|string $code = false): \HTMLPurifier_Language
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |
| `$code` | **bool&#124;string** | Code to override configuration with. Private parameter. |





***

### getFallbackFor

Returns the fallback language for language

```php
public getFallbackFor(string $code): string|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | language code |





***

### loadLanguage

Loads language into the cache, handles message file and fallbacks

```php
public loadLanguage(string $code): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | language code |





***


***
> Automatically generated on 2025-03-18
