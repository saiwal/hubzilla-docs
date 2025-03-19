
# BaseObject





* Full name: `\Zotlabs\Lib\BaseObject`



## Properties


### string



```php
public $string
```






***

### ldContext



```php
public $ldContext
```






***

## Methods


### __construct



```php
public __construct(mixed $input = null, mixed $strict = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$strict` | **mixed** |  |




**Throws:**
<p>if $strict</p>

- [`UnhandledElementException`](../ActivityStreams/UnhandledElementException.md)



***

### getDataType



```php
public getDataType(mixed $element, mixed $object = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** |  |
| `$object` | **mixed** |  |





***

### toArray



```php
public toArray(): mixed
```












***

### getLdContext



```php
public getLdContext(): mixed
```












***

### setLdContext



```php
public setLdContext(mixed $ldContext): \Zotlabs\Lib\BaseObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ldContext` | **mixed** |  |





***


***
> Automatically generated on 2025-03-19
