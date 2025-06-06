
# HTMLPurifier_Injector_RemoveSpansWithoutAttributes

Injector that removes spans with no attributes



* Full name: `\HTMLPurifier_Injector_RemoveSpansWithoutAttributes`
* Parent class: [`\HTMLPurifier_Injector`](./HTMLPurifier_Injector.md)



## Properties


### name

Advisory name of injector, this is for friendly error messages.

```php
public $name
```






***

### needed

Array of elements and attributes this injector creates and therefore
need to be allowed by the definition. Takes form of
array('element' => array('attr', 'attr2'), 'element2')

```php
public $needed
```






***

### attrValidator



```php
private $attrValidator
```






***

### config

Used by AttrValidator.

```php
private $config
```






***

### context



```php
private $context
```






***

### markForDeletion



```php
private $markForDeletion
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### prepare

Prepares the injector by giving it the config and context objects:
this allows references to important variables to be made within
the injector. This function also checks if the HTML environment
will work with the Injector (see checkNeeded()).

```php
public prepare(mixed $config, mixed $context): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **mixed** |  |
| `$context` | **mixed** |  |


**Return Value:**

Boolean false if success, string of missing needed element/attribute if failure




***

### handleElement

Handler that is called when a start or empty token is processed

```php
public handleElement(\HTMLPurifier_Token& $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token** |  |





***

### handleEnd

Handler that is called when an end token is processed

```php
public handleEnd(\HTMLPurifier_Token& $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token** |  |





***


## Inherited methods


### rewindOffset

Rewind to a spot to re-perform processing. This is useful if you
deleted a node, and now need to see if this change affected any
earlier nodes. Rewinding does not affect other injectors, and can
result in infinite loops if not used carefully.

```php
public rewindOffset(bool|int $offset): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **bool&#124;int** |  |





***

### getRewindOffset

Retrieves rewind offset, and then unsets it.

```php
public getRewindOffset(): bool|int
```












***

### prepare

Prepares the injector by giving it the config and context objects:
this allows references to important variables to be made within
the injector. This function also checks if the HTML environment
will work with the Injector (see checkNeeded()).

```php
public prepare(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

Boolean false if success, string of missing needed element/attribute if failure




***

### checkNeeded

This function checks if the HTML environment
will work with the Injector: if p tags are not allowed, the
Auto-Paragraphing injector should not be enabled.

```php
public checkNeeded(\HTMLPurifier_Config $config): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |


**Return Value:**

Boolean false if success, string of missing needed element/attribute if failure




***

### allowsElement

Tests if the context node allows a certain element

```php
public allowsElement(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Name of element to test for |


**Return Value:**

True if element is allowed, false if it is not




***

### forward

Iterator function, which starts with the next token and continues until
you reach the end of the input tokens.

```php
protected forward(int& $i, \HTMLPurifier_Token& $current): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **int** | Current integer index variable for inputTokens |
| `$current` | **\HTMLPurifier_Token** | Current token variable.<br />Do NOT use $token, as that variable is also a reference |





***

### forwardUntilEndToken

Similar to _forward, but accepts a third parameter $nesting (which
should be initialized at 0) and stops when we hit the end tag
for the node $this->inputIndex starts in.

```php
protected forwardUntilEndToken(int& $i, \HTMLPurifier_Token& $current, int& $nesting): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **int** | Current integer index variable for inputTokens |
| `$current` | **\HTMLPurifier_Token** | Current token variable.<br />Do NOT use $token, as that variable is also a reference |
| `$nesting` | **int** |  |





***

### backward

Iterator function, starts with the previous token and continues until
you reach the beginning of input tokens.

```php
protected backward(int& $i, \HTMLPurifier_Token& $current): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **int** | Current integer index variable for inputTokens |
| `$current` | **\HTMLPurifier_Token** | Current token variable.<br />Do NOT use $token, as that variable is also a reference |





***

### handleText

Handler that is called when a text token is processed

```php
public handleText(mixed& $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### handleElement

Handler that is called when a start or empty token is processed

```php
public handleElement(mixed& $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### handleEnd

Handler that is called when an end token is processed

```php
public handleEnd(mixed& $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### notifyEnd

Notifier that is called when an end token is processed

```php
public notifyEnd(\HTMLPurifier_Token $token): mixed
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token** | Current token variable. |





***


***
> Automatically generated on 2025-03-18
