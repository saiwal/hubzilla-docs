
# Smarty_Internal_ErrorHandler

Smarty error handler to fix new error levels in PHP8 for backwards compatibility



* Full name: `\Smarty_Internal_ErrorHandler`



## Properties


### allowUndefinedVars

Allows {$foo} where foo is unset.

```php
public bool $allowUndefinedVars
```






***

### allowUndefinedProperties

Allows {$foo->propName} where propName is undefined.

```php
public bool $allowUndefinedProperties
```






***

### allowUndefinedArrayKeys

Allows {$foo.bar} where bar is unset and {$foo.bar1.bar2} where either bar1 or bar2 is unset.

```php
public bool $allowUndefinedArrayKeys
```






***

### allowDereferencingNonObjects

Allows {$foo->bar} where bar is not an object (e.g. null or false).

```php
public bool $allowDereferencingNonObjects
```






***

### previousErrorHandler



```php
private $previousErrorHandler
```






***

## Methods


### activate

Enable error handler to intercept errors

```php
public activate(): mixed
```












***

### deactivate

Disable error handler

```php
public deactivate(): mixed
```












***

### handleError

Error Handler to mute expected messages

```php
public handleError(int $errno, mixed $errstr, mixed $errfile, mixed $errline, mixed $errcontext = []): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$errno` | **int** | Error level |
| `$errstr` | **mixed** |  |
| `$errfile` | **mixed** |  |
| `$errline` | **mixed** |  |
| `$errcontext` | **mixed** |  |





**See Also:**

* https://php.net/set_error_handler - 

***


***
> Automatically generated on 2025-03-15
