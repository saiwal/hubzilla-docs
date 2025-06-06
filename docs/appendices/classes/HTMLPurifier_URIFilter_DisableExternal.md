
# HTMLPurifier_URIFilter_DisableExternal

Chainable filters for custom URI processing.

These filters can perform custom actions on a URI filter object,
including transformation or blacklisting.  A filter named Foo
must have a corresponding configuration directive %URI.Foo,
unless always_load is specified to be true.

The following contexts may be available while URIFilters are being
processed:

     - EmbeddedURI: true if URI is an embedded resource that will
       be loaded automatically on page load
     - CurrentToken: a reference to the token that is currently
       being processed
     - CurrentAttr: the name of the attribute that is currently being
       processed
     - CurrentCSSProperty: the name of the CSS property that is
       currently being processed (if applicable)

* Full name: `\HTMLPurifier_URIFilter_DisableExternal`
* Parent class: [`\HTMLPurifier_URIFilter`](./HTMLPurifier_URIFilter.md)



## Properties


### name

Unique identifier of filter.

```php
public $name
```






***

### ourHostParts



```php
protected $ourHostParts
```






***

## Methods


### prepare

Performs initialization for the filter.  If the filter returns
false, this means that it shouldn't be considered active.

```php
public prepare(\HTMLPurifier_Config $config): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### filter

Filter a URI object

```php
public filter(\HTMLPurifier_URI& $uri, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **\HTMLPurifier_URI** | Reference |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


## Inherited methods


### prepare

Performs initialization for the filter.  If the filter returns
false, this means that it shouldn't be considered active.

```php
public prepare(\HTMLPurifier_Config $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### filter

Filter a URI object

```php
public filter(\HTMLPurifier_URI& $uri, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **\HTMLPurifier_URI** | Reference to URI object variable |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

Whether or not to continue processing: false indicates
URL is no good, true indicates continue processing. Note that
all changes are committed directly on the URI object




***


***
> Automatically generated on 2025-03-18
