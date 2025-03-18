
# SimplePie_Cache

Used to create cache objects



* Full name: `\SimplePie_Cache`
* Parent class: [`\SimplePie\Cache`](./SimplePie/Cache.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct

Don't call the constructor. Please.

```php
private __construct(): mixed
```












***

### get_handler

Create a new SimplePie\Cache object

```php
public static get_handler(string $location, string $filename, \SimplePie\Cache\Base::TYPE_FEED|\SimplePie\Cache\Base::TYPE_IMAGE $extension): \SimplePie\Cache\Base
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **string** | URL location (scheme is used to determine handler) |
| `$filename` | **string** | Unique identifier for cache object |
| `$extension` | **\SimplePie\Cache\Base::TYPE_FEED&#124;\SimplePie\Cache\Base::TYPE_IMAGE** | &#039;spi&#039; or &#039;spc&#039; |


**Return Value:**

Type of object depends on scheme of `$location`




***

### create

Create a new SimplePie\Cache object

```php
public create(mixed $location, mixed $filename, mixed $extension): mixed
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **mixed** |  |
| `$filename` | **mixed** |  |
| `$extension` | **mixed** |  |





***

### register

Register a handler

```php
public static register(string $type, class-string&lt;\SimplePie\Cache\Base&gt; $class): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | DSN type to register for |
| `$class` | **class-string<\SimplePie\Cache\Base>** | Name of handler class. Must implement Base |





***

### parse_URL

Parse a URL into an array

```php
public static parse_URL(string $url): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |





***


***
> Automatically generated on 2025-03-18
