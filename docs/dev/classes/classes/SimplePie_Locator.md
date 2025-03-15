
# SimplePie_Locator

Used for feed auto-discovery



* Full name: `\SimplePie_Locator`
* Parent class: [`\SimplePie\Locator`](./SimplePie/Locator.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


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
