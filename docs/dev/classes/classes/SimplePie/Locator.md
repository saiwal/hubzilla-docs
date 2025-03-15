***

# Locator

Used for feed auto-discovery

This class can be overloaded with {@see \SimplePie\SimplePie::set_locator_class()}

* Full name: `\SimplePie\Locator`
* This class implements:
[`\SimplePie\RegistryAware`](./RegistryAware.md)



## Properties


### useragent



```php
public $useragent
```






***

### timeout



```php
public $timeout
```






***

### file



```php
public $file
```






***

### local



```php
public $local
```






***

### elsewhere



```php
public $elsewhere
```






***

### cached_entities



```php
public $cached_entities
```






***

### http_base



```php
public $http_base
```






***

### base



```php
public $base
```






***

### base_location



```php
public $base_location
```






***

### checked_feeds



```php
public $checked_feeds
```






***

### max_checked_feeds



```php
public $max_checked_feeds
```






***

### force_fsockopen



```php
public $force_fsockopen
```






***

### curl_options



```php
public $curl_options
```






***

### dom



```php
public $dom
```






***

### registry



```php
protected $registry
```






***

## Methods


### __construct



```php
public __construct(\SimplePie\File $file, mixed $timeout = 10, mixed $useragent = null, mixed $max_checked_feeds = 10, mixed $force_fsockopen = false, mixed $curl_options = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **\SimplePie\File** |  |
| `$timeout` | **mixed** |  |
| `$useragent` | **mixed** |  |
| `$max_checked_feeds` | **mixed** |  |
| `$force_fsockopen` | **mixed** |  |
| `$curl_options` | **mixed** |  |





***

### set_registry

Set the Registry into the class

```php
public set_registry(\SimplePie\Registry $registry): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$registry` | **\SimplePie\Registry** |  |





***

### find



```php
public find(mixed $type = SimplePieSimplePie::LOCATOR_ALL, mixed& $working = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **mixed** |  |
| `$working` | **mixed** |  |





***

### is_feed



```php
public is_feed(mixed $file, mixed $check_html = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |
| `$check_html` | **mixed** |  |





***

### get_base



```php
public get_base(): mixed
```












***

### autodiscovery



```php
public autodiscovery(): mixed
```












***

### search_elements_by_tag



```php
protected search_elements_by_tag(mixed $name, mixed& $done, mixed $feeds): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$done` | **mixed** |  |
| `$feeds` | **mixed** |  |





***

### get_links



```php
public get_links(): mixed
```












***

### get_rel_link



```php
public get_rel_link(mixed $rel): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rel` | **mixed** |  |





***

### extension



```php
public extension(mixed& $array): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **mixed** |  |





***

### body



```php
public body(mixed& $array): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
