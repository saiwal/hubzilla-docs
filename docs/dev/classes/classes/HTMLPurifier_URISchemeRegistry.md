
# HTMLPurifier_URISchemeRegistry

Registry for retrieving specific URI scheme validator objects.



* Full name: `\HTMLPurifier_URISchemeRegistry`



## Properties


### schemes

Cache of retrieved schemes.

```php
protected $schemes
```






***

## Methods


### instance

Retrieve sole instance of the registry.

```php
public static instance(\HTMLPurifier_URISchemeRegistry $prototype = null): \HTMLPurifier_URISchemeRegistry
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **\HTMLPurifier_URISchemeRegistry** | Optional prototype to overload sole instance with,<br />or bool true to reset to default registry. |





***

### getScheme

Retrieves a scheme validator object

```php
public getScheme(string $scheme, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_URIScheme
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scheme` | **string** | String scheme name like http or mailto |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### register

Registers a custom scheme to the cache, bypassing reflection.

```php
public register(string $scheme, \HTMLPurifier_URIScheme $scheme_obj): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scheme` | **string** | Scheme name |
| `$scheme_obj` | **\HTMLPurifier_URIScheme** |  |





***


***
> Automatically generated on 2025-03-15
