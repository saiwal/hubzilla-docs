
# HTMLPurifier_URIScheme_https

Validates https (Secure HTTP) according to http scheme.



* Full name: `\HTMLPurifier_URIScheme_https`
* Parent class: [`\HTMLPurifier_URIScheme_http`](./HTMLPurifier_URIScheme_http.md)



## Properties


### default_port

Scheme's default port (integer). If an explicit port number is
specified that coincides with the default port, it will be
elided.

```php
public $default_port
```






***

### secure



```php
public $secure
```






***



## Inherited methods


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
