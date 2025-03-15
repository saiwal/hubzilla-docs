***

# HTMLPurifier_Lexer_DirectLex

Our in-house implementation of a parser.

A pure PHP parser, DirectLex has absolutely no dependencies, making
it a reasonably good default for PHP4.  Written with efficiency in mind,
it can be four times faster than HTMLPurifier_Lexer_PEARSax3, although it
pales in comparison to HTMLPurifier_Lexer_DOMLex.

* Full name: `\HTMLPurifier_Lexer_DirectLex`
* Parent class: [`\HTMLPurifier_Lexer`](./HTMLPurifier_Lexer.md)



## Properties


### tracksLineNumbers

Whether or not this lexer implements line-number/column-number tracking.

```php
public $tracksLineNumbers
```






***

### _whitespace

Whitespace characters for str(c)spn.

```php
protected $_whitespace
```






***

## Methods


### scriptCallback

Callback function for script CDATA fudge

```php
protected scriptCallback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** | , in form of array(opening tag, contents, closing tag) |





***

### tokenizeHTML

Lexes an HTML string into tokens.

```php
public tokenizeHTML(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): array|\HTMLPurifier_Token[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### substrCount

PHP 5.0.x compatible substr_count that implements offset and length

```php
protected substrCount(string $haystack, string $needle, int $offset, int $length): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$haystack` | **string** |  |
| `$needle` | **string** |  |
| `$offset` | **int** |  |
| `$length` | **int** |  |





***

### parseAttributeString

Takes the inside of an HTML tag and makes an assoc array of attributes.

```php
public parseAttributeString(string $string, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | Inside of tag excluding name. |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

Assoc array of attributes.




***


## Inherited methods


### create

Retrieves or sets the default Lexer as a Prototype Factory.

```php
public static create(\HTMLPurifier_Config $config): \HTMLPurifier_Lexer
```

By default HTMLPurifier_Lexer_DOMLex will be returned. There are
a few exceptions involving special features that only DirectLex
implements.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### __construct



```php
public __construct(): mixed
```












***

### parseText



```php
public parseText(mixed $string, mixed $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |
| `$config` | **mixed** |  |





***

### parseAttr



```php
public parseAttr(mixed $string, mixed $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |
| `$config` | **mixed** |  |





***

### parseData

Parses special entities into the proper characters.

```php
public parseData(string $string, mixed $is_attr, mixed $config): string
```

This string will translate escaped versions of the special characters
into the correct ones.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String character data to be parsed. |
| `$is_attr` | **mixed** |  |
| `$config` | **mixed** |  |


**Return Value:**

Parsed character data.




***

### tokenizeHTML

Lexes an HTML string into tokens.

```php
public tokenizeHTML(mixed $string, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_Token[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** | String HTML. |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

array representation of HTML.




***

### escapeCDATA

Translates CDATA sections into regular sections (through escaping).

```php
protected static escapeCDATA(string $string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | HTML string to process. |


**Return Value:**

HTML with CDATA sections escaped.




***

### escapeCommentedCDATA

Special CDATA case that is especially convoluted for <script>

```php
protected static escapeCommentedCDATA(string $string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | HTML string to process. |


**Return Value:**

HTML with CDATA sections escaped.




***

### removeIEConditional

Special Internet Explorer conditional comments should be removed.

```php
protected static removeIEConditional(string $string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | HTML string to process. |


**Return Value:**

HTML with conditional comments removed.




***

### CDATACallback

Callback function for escapeCDATA() that does the work.

```php
protected static CDATACallback(array $matches): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** | PCRE matches array, with index 0 the entire match<br />and 1 the inside of the CDATA section. |


**Return Value:**

Escaped internals of the CDATA section.




***

### normalize

Takes a piece of HTML and normalizes it by converting entities, fixing
encoding, extracting bits, and other good stuff.

```php
public normalize(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** | HTML. |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### extractBody

Takes a string of HTML (fragment or document) and returns the content

```php
public extractBody(mixed $html): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
