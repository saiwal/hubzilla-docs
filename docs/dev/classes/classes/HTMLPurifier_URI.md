
# HTMLPurifier_URI

HTML Purifier's internal representation of a URI.



* Full name: `\HTMLPurifier_URI`



## Properties


### scheme



```php
public $scheme
```






***

### userinfo



```php
public $userinfo
```






***

### host



```php
public $host
```






***

### port



```php
public $port
```






***

### path



```php
public $path
```






***

### query



```php
public $query
```






***

### fragment



```php
public $fragment
```






***

## Methods


### __construct



```php
public __construct(string $scheme, string $userinfo, string $host, int $port, string $path, string $query, string $fragment): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scheme` | **string** |  |
| `$userinfo` | **string** |  |
| `$host` | **string** |  |
| `$port` | **int** |  |
| `$path` | **string** |  |
| `$query` | **string** |  |
| `$fragment` | **string** |  |





***

### getSchemeObj

Retrieves a scheme object corresponding to the URI's scheme/default

```php
public getSchemeObj(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_URIScheme
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

Scheme object appropriate for validating this URI




***

### validate

Generic validation method applicable for all schemes. May modify
this URI in order to get it into a compliant form.

```php
public validate(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

True if validation/filtering succeeds, false if failure




***

### toString

Convert URI back to string

```php
public toString(): string
```









**Return Value:**

URI appropriate for output




***

### isLocal

Returns true if this URL might be considered a 'local' URL given
the current context.  This is true when the host is null, or
when it matches the host supplied to the configuration.

```php
public isLocal(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```

Note that this does not do any scheme checking, so it is mostly
only appropriate for metadata that doesn't care about protocol
security.  isBenign is probably what you actually want.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### isBenign

Returns true if this URL should be considered a 'benign' URL,
that is:

```php
public isBenign(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```

- It is a local URL (isLocal), and
- It has a equal or better level of security






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


***
> Automatically generated on 2025-03-15
