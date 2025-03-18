
# HTMLPurifier_URIScheme_file

Validates file as defined by RFC 1630 and RFC 1738.



* Full name: `\HTMLPurifier_URIScheme_file`
* Parent class: [`\HTMLPurifier_URIScheme`](./HTMLPurifier_URIScheme.md)



## Properties


### browsable

Generally file:// URLs are not accessible from most
machines, so placing them as an img src is incorrect.

```php
public $browsable
```






***

### may_omit_host

Basically the *only* URI scheme for which this is true, since
accessing files on the local machine is very common.  In fact,
browsers on some operating systems don't understand the
authority, though I hear it is used on Windows to refer to
network shares.

```php
public $may_omit_host
```






***

## Methods


### doValidate

Validates the components of a URI for a specific scheme.

```php
public doValidate(\HTMLPurifier_URI& $uri, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **\HTMLPurifier_URI** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


## Inherited methods


### doValidate

Validates the components of a URI for a specific scheme.

```php
public doValidate(\HTMLPurifier_URI& $uri, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **\HTMLPurifier_URI** | Reference to a HTMLPurifier_URI object |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

success or failure




***

### validate

Public interface for validating components of a URI.  Performs a
bunch of default actions. Don't overload this method.

```php
public validate(\HTMLPurifier_URI& $uri, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **\HTMLPurifier_URI** | Reference to a HTMLPurifier_URI object |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

success or failure




***


***
> Automatically generated on 2025-03-18
