
# HTMLPurifier_Definition

Super-class for definition datatype objects, implements serialization
functions for the class.



* Full name: `\HTMLPurifier_Definition`
* This class is an **Abstract class**



## Properties


### setup

Has setup() been called yet?

```php
public $setup
```






***

### optimized

If true, write out the final definition object to the cache after
setup.  This will be true only if all invocations to get a raw
definition object are also optimized.  This does not cause file
system thrashing because on subsequent calls the cached object
is used and any writes to the raw definition object are short
circuited.  See enduser-customize.html for the high-level
picture.

```php
public $optimized
```






***

### type

What type of definition is it?

```php
public $type
```






***

## Methods


### doSetup

Sets up the definition object into the final form, something
not done by the constructor

```php
protected doSetup(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### setup

Setup function that aborts if already setup

```php
public setup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


***
> Automatically generated on 2025-03-18
