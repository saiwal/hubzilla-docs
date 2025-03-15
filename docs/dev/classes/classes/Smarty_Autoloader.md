***

# Smarty_Autoloader

Smarty Autoloader



* Full name: `\Smarty_Autoloader`



## Properties


### SMARTY_DIR

Filepath to Smarty root

```php
public static string $SMARTY_DIR
```



* This property is **static**.


***

### SMARTY_SYSPLUGINS_DIR

Filepath to Smarty internal plugins

```php
public static string $SMARTY_SYSPLUGINS_DIR
```



* This property is **static**.


***

### rootClasses

Array with Smarty core classes and their filename

```php
public static array $rootClasses
```



* This property is **static**.


***

## Methods


### registerBC

Registers Smarty_Autoloader backward compatible to older installations.

```php
public static registerBC(bool $prepend = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prepend` | **bool** | Whether to prepend the autoloader or not. |





***

### register

Registers Smarty_Autoloader as an SPL autoloader.

```php
public static register(bool $prepend = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prepend` | **bool** | Whether to prepend the autoloader or not. |





***

### autoload

Handles auto loading of classes.

```php
public static autoload(string $class): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | A class name. |





***


***
> Automatically generated on 2025-03-15
