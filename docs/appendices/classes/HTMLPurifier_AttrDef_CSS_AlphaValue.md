
# HTMLPurifier_AttrDef_CSS_AlphaValue

Validates a number as defined by the CSS spec.



* Full name: `\HTMLPurifier_AttrDef_CSS_AlphaValue`
* Parent class: [`\HTMLPurifier_AttrDef_CSS_Number`](./HTMLPurifier_AttrDef_CSS_Number.md)




## Methods


### __construct



```php
public __construct(): mixed
```












***

### validate

Validates and cleans passed string according to a definition.

```php
public validate(string $number, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


## Inherited methods


### validate

Validates and cleans passed string according to a definition.

```php
public validate(string $number, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** |  |
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

### __construct



```php
public __construct(bool $non_negative = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$non_negative` | **bool** | indicates whether negatives are forbidden |





***


***
> Automatically generated on 2025-03-18
