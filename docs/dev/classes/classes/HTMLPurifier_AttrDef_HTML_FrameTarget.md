
# HTMLPurifier_AttrDef_HTML_FrameTarget

Special-case enum attribute definition that lazy loads allowed frame targets



* Full name: `\HTMLPurifier_AttrDef_HTML_FrameTarget`
* Parent class: [`\HTMLPurifier_AttrDef_Enum`](./HTMLPurifier_AttrDef_Enum.md)



## Properties


### valid_values

Lookup table of valid values.

```php
public $valid_values
```






***

### case_sensitive

Bool indicating whether or not enumeration is case sensitive.

```php
protected $case_sensitive
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### validate

Validates and cleans passed string according to a definition.

```php
public validate(string $string, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


## Inherited methods


### validate

Validates and cleans passed string according to a definition.

```php
public validate(string $string, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





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
public make(string $string): \HTMLPurifier_AttrDef_Enum
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | In form of comma-delimited list of case-insensitive<br />valid values. Example: &quot;foo,bar,baz&quot;. Prepend &quot;s:&quot; to make<br />case sensitive |





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

### __construct



```php
public __construct(array $valid_values = array(), bool $case_sensitive = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$valid_values` | **array** | List of valid values |
| `$case_sensitive` | **bool** | Whether or not case sensitive |





***


***
> Automatically generated on 2025-03-15
