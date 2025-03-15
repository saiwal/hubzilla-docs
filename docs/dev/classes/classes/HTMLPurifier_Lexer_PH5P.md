***

# HTMLPurifier_Lexer_PH5P

Experimental HTML5-based parser using Jeroen van der Meer's PH5P library.

Occupies space in the HTML5 pseudo-namespace, which may cause conflicts.

* Full name: `\HTMLPurifier_Lexer_PH5P`
* Parent class: [`\HTMLPurifier_Lexer_DOMLex`](./HTMLPurifier_Lexer_DOMLex.md)




## Methods


### tokenizeHTML

Lexes an HTML string into tokens.

```php
public tokenizeHTML(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_Token[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





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
public tokenizeHTML(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_Token[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





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

### tokenizeDOM

Iterative function that tokenizes a node, putting it into an accumulator.

```php
protected tokenizeDOM(\DOMNode $node, \HTMLPurifier_Token[]& $tokens, mixed $config): mixed
```

To iterate is human, to recurse divine - L. Peter Deutsch






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\DOMNode** | DOMNode to be tokenized. |
| `$tokens` | **\HTMLPurifier_Token[]** | Array-list of already tokenized tokens. |
| `$config` | **mixed** |  |





***

### getTagName

Portably retrieve the tag name of a node; deals with older versions
of libxml like 2.7.6

```php
protected getTagName(\DOMNode $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\DOMNode** |  |





***

### getData

Portably retrieve the data of a node; deals with older versions
of libxml like 2.7.6

```php
protected getData(\DOMNode $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\DOMNode** |  |





***

### createStartNode



```php
protected createStartNode(\DOMNode $node, \HTMLPurifier_Token[]& $tokens, bool $collect, mixed $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\DOMNode** | DOMNode to be tokenized. |
| `$tokens` | **\HTMLPurifier_Token[]** | Array-list of already tokenized tokens. |
| `$collect` | **bool** | Says whether or start and close are collected, set to<br />false at first recursion because it&#039;s the implicit DIV<br />tag you&#039;re dealing with. |
| `$config` | **mixed** |  |


**Return Value:**

if the token needs an endtoken




***

### createEndNode



```php
protected createEndNode(\DOMNode $node, \HTMLPurifier_Token[]& $tokens): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\DOMNode** |  |
| `$tokens` | **\HTMLPurifier_Token[]** |  |





***

### transformAttrToAssoc

Converts a DOMNamedNodeMap of DOMAttr objects into an assoc array.

```php
protected transformAttrToAssoc(\DOMNamedNodeMap $node_map): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node_map` | **\DOMNamedNodeMap** | DOMNamedNodeMap of DOMAttr objects. |


**Return Value:**

Associative array of attributes.




***

### muteErrorHandler

An error handler that mutes all errors

```php
public muteErrorHandler(int $errno, string $errstr): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$errno` | **int** |  |
| `$errstr` | **string** |  |





***

### callbackUndoCommentSubst

Callback function for undoing escaping of stray angled brackets
in comments

```php
public callbackUndoCommentSubst(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### callbackArmorCommentEntities

Callback function that entity-izes ampersands in comments so that
callbackUndoCommentSubst doesn't clobber them

```php
public callbackArmorCommentEntities(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### wrapHTML

Wraps an HTML fragment in the necessary HTML

```php
protected wrapHTML(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context, mixed $use_div = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |
| `$use_div` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
