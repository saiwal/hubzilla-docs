***

# HTMLPurifier_DoctypeRegistry





* Full name: `\HTMLPurifier_DoctypeRegistry`



## Properties


### doctypes

Hash of doctype names to doctype objects.

```php
protected $doctypes
```






***

### aliases

Lookup table of aliases to real doctype names.

```php
protected $aliases
```






***

## Methods


### register

Registers a doctype to the registry

```php
public register(string $doctype, bool $xml = true, array $modules = array(), array $tidy_modules = array(), array $aliases = array(), string $dtd_public = null, string $dtd_system = null): \HTMLPurifier_Doctype
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$doctype` | **string** | Name of doctype or literal doctype object |
| `$xml` | **bool** |  |
| `$modules` | **array** | Modules doctype will load |
| `$tidy_modules` | **array** | Modules doctype will load for certain modes |
| `$aliases` | **array** | Alias names for doctype |
| `$dtd_public` | **string** |  |
| `$dtd_system` | **string** |  |


**Return Value:**

Editable registered doctype




***

### get

Retrieves reference to a doctype of a certain name

```php
public get(string $doctype): \HTMLPurifier_Doctype
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$doctype` | **string** | Name of doctype |


**Return Value:**

Editable doctype object




***

### make

Creates a doctype based on a configuration object,
will perform initialization on the doctype

```php
public make(\HTMLPurifier_Config $config): \HTMLPurifier_Doctype
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### getDoctypeFromConfig

Retrieves the doctype from the configuration object

```php
public getDoctypeFromConfig(\HTMLPurifier_Config $config): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


***
> Automatically generated on 2025-03-15
