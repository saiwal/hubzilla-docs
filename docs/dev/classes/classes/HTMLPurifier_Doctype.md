
# HTMLPurifier_Doctype

Represents a document type, contains information on which modules
need to be loaded.



* Full name: `\HTMLPurifier_Doctype`



## Properties


### name

Full name of doctype

```php
public $name
```






***

### modules

List of standard modules (string identifiers or literal objects)
that this doctype uses

```php
public $modules
```






***

### tidyModules

List of modules to use for tidying up code

```php
public $tidyModules
```






***

### xml

Is the language derived from XML (i.e. XHTML)?

```php
public $xml
```






***

### aliases

List of aliases for this doctype

```php
public $aliases
```






***

### dtdPublic

Public DTD identifier

```php
public $dtdPublic
```






***

### dtdSystem

System DTD identifier

```php
public $dtdSystem
```






***

## Methods


### __construct



```php
public __construct(mixed $name = null, mixed $xml = true, mixed $modules = array(), mixed $tidyModules = array(), mixed $aliases = array(), mixed $dtd_public = null, mixed $dtd_system = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$xml` | **mixed** |  |
| `$modules` | **mixed** |  |
| `$tidyModules` | **mixed** |  |
| `$aliases` | **mixed** |  |
| `$dtd_public` | **mixed** |  |
| `$dtd_system` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
