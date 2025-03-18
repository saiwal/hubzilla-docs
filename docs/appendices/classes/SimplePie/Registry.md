
# Registry

Handles creating objects and calling methods

Access this via {@see \SimplePie\SimplePie::get_registry()}

* Full name: `\SimplePie\Registry`



## Properties


### default

Default class mapping

```php
protected array&lt;class-string,class-string&gt; $default
```

Overriding classes *must* subclass these.




***

### classes

Class mapping

```php
protected array $classes
```





**See Also:**

* \SimplePie\register() - 

***

### legacy

Legacy classes

```php
protected class-string[] $legacy
```





**See Also:**

* \SimplePie\register() - 

***

### legacyTypes

Legacy types

```php
private array&lt;string,class-string&gt; $legacyTypes
```





**See Also:**

* \SimplePie\register() - 

***

## Methods


### __construct

Constructor

```php
public __construct(): mixed
```

No-op










***

### register

Register a class

```php
public register(string $type, class-string $class, bool $legacy = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | See {@see $default} for names |
| `$class` | **class-string** | Class name, must subclass the corresponding default |
| `$legacy` | **bool** | Whether to enable legacy support for this class |


**Return Value:**

Successfulness




***

### get_class

Get the class registered for a type

```php
public get_class(class-string&lt;\SimplePie\T&gt; $type): class-string&lt;\SimplePie\T&gt;|null
```

Where possible, use {@see \SimplePie\create()} or {@see \SimplePie\call()} instead






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **class-string<\SimplePie\T>** |  |





***

### create

Create a new instance of a given type

```php
public create(class-string&lt;\SimplePie\T&gt; $type, array $parameters = []): \SimplePie\T
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **class-string<\SimplePie\T>** |  |
| `$parameters` | **array** | Parameters to pass to the constructor |


**Return Value:**

Instance of class




***

### call

Call a static method for a type

```php
public call(class-string $type, string $method, array $parameters = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **class-string** |  |
| `$method` | **string** |  |
| `$parameters` | **array** |  |





***


***
> Automatically generated on 2025-03-18
