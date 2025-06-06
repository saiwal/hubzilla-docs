
# HTMLPurifier_AttrDef_URI_IPv4

Validates an IPv4 address



* Full name: `\HTMLPurifier_AttrDef_URI_IPv4`
* Parent class: [`\HTMLPurifier_AttrDef`](./HTMLPurifier_AttrDef.md)



## Properties


### ip4

IPv4 regex, protected so that IPv6 can reuse it.

```php
protected $ip4
```






***

## Methods


### validate

Validates and cleans passed string according to a definition.

```php
public validate(string $aIP, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$aIP` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### _loadRegex

Lazy load function to prevent regex from being stuffed in
cache.

```php
protected _loadRegex(): mixed
```












***


## Inherited methods


### validate

Validates and cleans passed string according to a definition.

```php
public validate(string $string, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to be validated and cleaned. |
| `$config` | **\HTMLPurifier_Config** | Mandatory HTMLPurifier_Config object. |
| `$context` | **\HTMLPurifier_Context** | Mandatory HTMLPurifier_Context object. |





***

### parseCDATA

Convenience method that parses a string as if it were CDATA.

```php
public parseCDATA(mixed $string): mixed
```

This method process a string in the manner specified at
<http://www.w3.org/TR/html4/types.html#h-6.2> by removing
leading and trailing whitespace, ignoring line feeds, and replacing
carriage returns and tabs with spaces.  While most useful for HTML
attributes specified as CDATA, it can also be applied to most CSS
values.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### make

Factory method for creating this class from a string.

```php
public make(string $string): \HTMLPurifier_AttrDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String construction info |


**Return Value:**

Created AttrDef object corresponding to $string




***

### mungeRgb

Removes spaces from rgb(0, 0, 0) so that shorthand CSS properties work
properly. THIS IS A HACK!

```php
protected mungeRgb(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | a CSS colour definition |





***

### expandCSSEscape

Parses a possibly escaped CSS string and returns the "pure"
version of it.

```php
protected expandCSSEscape(mixed $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
