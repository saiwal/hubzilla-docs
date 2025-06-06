
# HTMLPurifier_AttrDef_Integer

Validates an integer.



* Full name: `\HTMLPurifier_AttrDef_Integer`
* Parent class: [`\HTMLPurifier_AttrDef`](./HTMLPurifier_AttrDef.md)



## Properties


### negative

Whether or not negative values are allowed.

```php
protected $negative
```






***

### zero

Whether or not zero is allowed.

```php
protected $zero
```






***

### positive

Whether or not positive values are allowed.

```php
protected $positive
```






***

## Methods


### __construct



```php
public __construct(mixed $negative = true, mixed $zero = true, mixed $positive = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$negative` | **mixed** | Bool indicating whether or not negative values are allowed |
| `$zero` | **mixed** | Bool indicating whether or not zero is allowed |
| `$positive` | **mixed** | Bool indicating whether or not positive values are allowed |





***

### validate

Validates and cleans passed string according to a definition.

```php
public validate(string $integer, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$integer` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





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
