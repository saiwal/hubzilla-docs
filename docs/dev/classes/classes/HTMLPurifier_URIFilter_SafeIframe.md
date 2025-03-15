***

# HTMLPurifier_URIFilter_SafeIframe

Implements safety checks for safe iframes.



* Full name: `\HTMLPurifier_URIFilter_SafeIframe`
* Parent class: [`\HTMLPurifier_URIFilter`](./HTMLPurifier_URIFilter.md)



## Properties


### name

Unique identifier of filter.

```php
public $name
```






***

### always_load

True if this filter should always be loaded.

```php
public $always_load
```






***

### regexp



```php
protected $regexp
```






***

## Methods


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








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **\HTMLPurifier_URI** |  |
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
> Automatically generated on 2025-03-15
