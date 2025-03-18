
# HTMLPurifier_DefinitionCacheFactory

Responsible for creating definition caches.



* Full name: `\HTMLPurifier_DefinitionCacheFactory`



## Properties


### caches



```php
protected $caches
```






***

### implementations



```php
protected $implementations
```






***

### decorators



```php
protected $decorators
```






***

## Methods


### setup

Initialize default decorators

```php
public setup(): mixed
```












***

### instance

Retrieves an instance of global definition cache factory.

```php
public static instance(\HTMLPurifier_DefinitionCacheFactory $prototype = null): \HTMLPurifier_DefinitionCacheFactory
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **\HTMLPurifier_DefinitionCacheFactory** |  |





***

### register

Registers a new definition cache object

```php
public register(string $short, string $long): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$short` | **string** | Short name of cache object, for reference |
| `$long` | **string** | Full class name of cache object, for construction |





***

### create

Factory method that creates a cache object based on configuration

```php
public create(string $type, \HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | Name of definitions handled by cache |
| `$config` | **\HTMLPurifier_Config** | Config instance |





***

### addDecorator

Registers a decorator to add to all new cache objects

```php
public addDecorator(\HTMLPurifier_DefinitionCache_Decorator|string $decorator): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$decorator` | **\HTMLPurifier_DefinitionCache_Decorator&#124;string** | An instance or the name of a decorator |





***


***
> Automatically generated on 2025-03-18
