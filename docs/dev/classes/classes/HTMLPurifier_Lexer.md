
# HTMLPurifier_Lexer

Forgivingly lexes HTML (SGML-style) markup into tokens.

A lexer parses a string of SGML-style markup and converts them into
corresponding tokens.  It doesn't check for well-formedness, although its
internal mechanism may make this automatic (such as the case of
HTMLPurifier_Lexer_DOMLex).  There are several implementations to choose
from.

A lexer is HTML-oriented: it might work with XML, but it's not
recommended, as we adhere to a subset of the specification for optimization
reasons. This might change in the future. Also, most tokenizers are not
expected to handle DTDs or PIs.

This class should not be directly instantiated, but you may use create() to
retrieve a default copy of the lexer.  Being a supertype, this class
does not actually define any implementation, but offers commonly used
convenience functions for subclasses.

* Full name: `\HTMLPurifier_Lexer`



## Properties


### tracksLineNumbers

Whether or not this lexer implements line-number/column-number tracking.

```php
public $tracksLineNumbers
```

If it does, set to true.




***

### _entity_parser



```php
private $_entity_parser
```






***

### _special_entity2str

Most common entity to raw value conversion table for special entities.

```php
protected $_special_entity2str
```






***

## Methods


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
