
# HTMLPurifier_Bootstrap

Bootstrap class that contains meta-functionality for HTML Purifier such as
the autoload function.



* Full name: `\HTMLPurifier_Bootstrap`




## Methods


### autoload

Autoload function for HTML Purifier

```php
public static autoload(string $class): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Class to load |





***

### getPath

Returns the path for a specific class.

```php
public static getPath(string $class): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Class path to get |





***

### registerAutoload

"Pre-registers" our autoloader on the SPL stack.

```php
public static registerAutoload(): mixed
```



* This method is **static**.








***


***
> Automatically generated on 2025-03-15
