
# HTMLPurifier_Generator

Generates HTML from tokens.



* Full name: `\HTMLPurifier_Generator`



## Properties


### _xhtml

Whether or not generator should produce XML output.

```php
private $_xhtml
```






***

### _scriptFix

:HACK: Whether or not generator should comment the insides of <script> tags.

```php
private $_scriptFix
```






***

### _def

Cache of HTMLDefinition during HTML output to determine whether or
not attributes should be minimized.

```php
private $_def
```






***

### _sortAttr

Cache of %Output.SortAttr.

```php
private $_sortAttr
```






***

### _flashCompat

Cache of %Output.FlashCompat.

```php
private $_flashCompat
```






***

### _innerHTMLFix

Cache of %Output.FixInnerHTML.

```php
private $_innerHTMLFix
```






***

### _flashStack

Stack for keeping track of object information when outputting IE
compatibility code.

```php
private $_flashStack
```






***

### config

Configuration for the generator

```php
protected $config
```






***

## Methods


### __construct



```php
public __construct(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### generateFromTokens

Generates HTML from an array of tokens.

```php
public generateFromTokens(\HTMLPurifier_Token[] $tokens): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokens` | **\HTMLPurifier_Token[]** | Array of HTMLPurifier_Token |


**Return Value:**

Generated HTML




***

### generateFromToken

Generates HTML from a single token.

```php
public generateFromToken(\HTMLPurifier_Token $token): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token** | HTMLPurifier_Token object. |


**Return Value:**

Generated HTML




***

### generateScriptFromToken

Special case processor for the contents of script tags

```php
public generateScriptFromToken(\HTMLPurifier_Token $token): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token** | HTMLPurifier_Token object. |





***

### generateAttributes

Generates attribute declarations from attribute array.

```php
public generateAttributes(array $assoc_array_of_attributes, string $element = &#039;&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$assoc_array_of_attributes` | **array** | Attribute array |
| `$element` | **string** | Name of element attributes are for, used to check<br />attribute minimization. |


**Return Value:**

Generated HTML fragment for insertion.




***

### escape

Escapes raw text data.

```php
public escape(string $string, int $quote = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String data to escape for HTML. |
| `$quote` | **int** | Quoting style, like htmlspecialchars. ENT_NOQUOTES is<br />permissible for non-attribute output. |


**Return Value:**

escaped data.




***


***
> Automatically generated on 2025-03-18
