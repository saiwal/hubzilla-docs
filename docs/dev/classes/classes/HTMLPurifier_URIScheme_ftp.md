
# HTMLPurifier_URIScheme_ftp

Validates ftp (File Transfer Protocol) URIs as defined by generic RFC 1738.



* Full name: `\HTMLPurifier_URIScheme_ftp`
* Parent class: [`\HTMLPurifier_URIScheme`](./HTMLPurifier_URIScheme.md)



## Properties


### default_port

Scheme's default port (integer). If an explicit port number is
specified that coincides with the default port, it will be
elided.

```php
public $default_port
```






***

### browsable

Whether or not URIs of this scheme are locatable by a browser
http and ftp are accessible, while mailto and news are not.

```php
public $browsable
```






***

### hierarchical

Whether or not the URI always uses <hier_part>, resolves edge cases
with making relative URIs absolute

```php
public $hierarchical
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
> Automatically generated on 2025-03-15
