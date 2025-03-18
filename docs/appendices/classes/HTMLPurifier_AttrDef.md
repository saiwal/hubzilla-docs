
# HTMLPurifier_AttrDef

Base class for all validating attribute definitions.

This family of classes forms the core for not only HTML attribute validation,
but also any sort of string that needs to be validated or cleaned (which
means CSS properties and composite definitions are defined here too).
Besides defining (through code) what precisely makes the string valid,
subclasses are also responsible for cleaning the code if possible.

* Full name: `\HTMLPurifier_AttrDef`
* This class is an **Abstract class**



## Properties


### minimized

Tells us whether or not an HTML attribute is minimized.

```php
public $minimized
```

Has no meaning in other contexts.




***

### required

Tells us whether or not an HTML attribute is required.

```php
public $required
```

Has no meaning in other contexts




***

## Methods


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
