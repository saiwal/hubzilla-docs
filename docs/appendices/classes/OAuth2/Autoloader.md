
# Autoloader

Autoloads OAuth2 classes



* Full name: `\OAuth2\Autoloader`



## Properties


### dir



```php
private string $dir
```






***

## Methods


### __construct



```php
public __construct(string $dir = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |





***

### register

Registers OAuth2\Autoloader as an SPL autoloader.

```php
public static register(mixed $dir = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **mixed** |  |





***

### autoload

Handles autoloading of classes.

```php
public autoload(string $class): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | - A class name. |





***


***
> Automatically generated on 2025-03-18
