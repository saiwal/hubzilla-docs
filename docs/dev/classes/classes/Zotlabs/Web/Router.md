
# Router

We have already parsed the server path into App::$argc and App::$argv

App::$argv[0] is our module name. Let's call it 'foo'. We will load the
Zotlabs/Module/Foo.php (object) or file mod/foo.php (procedural)
and use it for handling our URL request to 'https://ourgreatwebsite.something/foo' .
The module file contains a few functions that we call in various circumstances
and in the following order:

* Full name: `\Zotlabs\Web\Router`



## Properties


### modname



```php
private $modname
```






***

### controller



```php
private $controller
```






***

### module_loaded



```php
private bool $module_loaded
```






***

## Methods


### __construct



```php
public __construct(): mixed
```











**Throws:**
<p>module not found</p>

- [`Exception`](../../Exception.md)



***

### Dispatch



```php
public Dispatch(): mixed
```












***


***
> Automatically generated on 2025-03-15
