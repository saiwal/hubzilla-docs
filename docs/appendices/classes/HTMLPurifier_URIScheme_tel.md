
# HTMLPurifier_URIScheme_tel

Validates tel (for phone numbers).

The relevant specifications for this protocol are RFC 3966 and RFC 5341,
but this class takes a much simpler approach: we normalize phone
numbers so that they only include (possibly) a leading plus,
and then any number of digits and x'es.

* Full name: `\HTMLPurifier_URIScheme_tel`
* Parent class: [`\HTMLPurifier_URIScheme`](./HTMLPurifier_URIScheme.md)



## Properties


### browsable

Whether or not URIs of this scheme are locatable by a browser
http and ftp are accessible, while mailto and news are not.

```php
public $browsable
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
