***

# Warn





* Full name: `\ScssPhp\ScssPhp\Warn`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### callback



```php
private static callable|null $callback
```



* This property is **static**.


***

## Methods


### warning

Prints a warning message associated with the current `@import` or function call.

```php
public static warning(string $message): void
```

This may only be called within a custom function or importer callback.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |





***

### deprecation

Prints a deprecation warning message associated with the current `@import` or function call.

```php
public static deprecation(string $message): void
```

This may only be called within a custom function or importer callback.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |





***

### reportWarning



```php
private static reportWarning(string $message, bool $deprecation): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |
| `$deprecation` | **bool** |  |





***


***
> Automatically generated on 2025-03-15
