***

# HTMLPurifier_URIScheme

Validator for the components of a URI for a specific scheme



* Full name: `\HTMLPurifier_URIScheme`
* This class is an **Abstract class**



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

### secure

Whether or not data transmitted over this scheme is encrypted.

```php
public $secure
```

https is secure, http is not.




***

### hierarchical

Whether or not the URI always uses <hier_part>, resolves edge cases
with making relative URIs absolute

```php
public $hierarchical
```






***

### may_omit_host

Whether or not the URI may omit a hostname when the scheme is
explicitly specified, ala file:///path/to/file. As of writing,
'file' is the only scheme that browsers support his properly.

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
