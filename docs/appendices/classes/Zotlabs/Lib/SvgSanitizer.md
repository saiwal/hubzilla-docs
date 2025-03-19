
# SvgSanitizer

SVGSantiizer

Whitelist-based PHP SVG sanitizer.

* Full name: `\Zotlabs\Lib\SvgSanitizer`

**See Also:**

* https://github.com/alister-/SVG-Sanitizer} - @author Alister Norris
@copyright Copyright (c) 2013 Alister Norris
@license http://opensource.org/licenses/mit-license.php The MIT License
@package svgsanitizer



## Properties


### xmlDoc



```php
private $xmlDoc
```






***

### removedattrs



```php
private $removedattrs
```






***

### allowed_functions



```php
private static $allowed_functions
```



* This property is **static**.


***

### whitelist



```php
private static $whitelist
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### load



```php
public load(mixed $file): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |





***

### loadXML



```php
public loadXML(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### sanitize



```php
public sanitize(): mixed
```












***

### saveSVG



```php
public saveSVG(): mixed
```












***


***
> Automatically generated on 2025-03-19
