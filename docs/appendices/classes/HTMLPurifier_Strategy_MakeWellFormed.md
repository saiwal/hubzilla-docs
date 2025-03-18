
# HTMLPurifier_Strategy_MakeWellFormed

Takes tokens makes them well-formed (balance end tags, etc.)

Specification of the armor attributes this strategy uses:

- MakeWellFormed_TagClosedError: This armor field is used to
  suppress tag closed errors for certain tokens [TagClosedSuppress],
  in particular, if a tag was generated automatically by HTML
  Purifier, we may rely on our infrastructure to close it for us
  and shouldn't report an error to the user [TagClosedAuto].

* Full name: `\HTMLPurifier_Strategy_MakeWellFormed`
* Parent class: [`\HTMLPurifier_Strategy`](./HTMLPurifier_Strategy.md)



## Properties


### tokens

Array stream of tokens being processed.

```php
protected $tokens
```






***

### token

Current token.

```php
protected $token
```






***

### zipper

Zipper managing the true state.

```php
protected $zipper
```






***

### stack

Current nesting of elements.

```php
protected $stack
```






***

### injectors

Injectors active in this stream processing.

```php
protected $injectors
```






***

### config

Current instance of HTMLPurifier_Config.

```php
protected $config
```






***

### context

Current instance of HTMLPurifier_Context.

```php
protected $context
```






***

## Methods


### execute

Executes the strategy on the tokens.

```php
public execute(\HTMLPurifier_Token[] $tokens, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_Token[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokens` | **\HTMLPurifier_Token[]** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### processToken

Processes arbitrary token values for complicated substitution patterns.

```php
protected processToken(\HTMLPurifier_Token|array|int|bool $token, \HTMLPurifier_Injector|int $injector = -1): mixed
```

In general:

If $token is an array, it is a list of tokens to substitute for the
current token. These tokens then get individually processed. If there
is a leading integer in the list, that integer determines how many
tokens from the stream should be removed.

If $token is a regular token, it is swapped with the current token.

If $token is false, the current token is deleted.

If $token is an integer, that number of tokens (with the first token
being the current one) will be deleted.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token&#124;array&#124;int&#124;bool** | Token substitution value |
| `$injector` | **\HTMLPurifier_Injector&#124;int** | Injector that performed the substitution; default is if<br />this is not an injector related operation. |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### insertBefore

Inserts a token before the current token. Cursor now points to
this token.  You must reprocess after this.

```php
private insertBefore(\HTMLPurifier_Token $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token** |  |





***

### remove

Removes current token. Cursor now points to new token occupying previously
occupied space.  You must reprocess after this.

```php
private remove(): mixed
```












***


## Inherited methods


### execute

Executes the strategy on the tokens.

```php
public execute(\HTMLPurifier_Token[] $tokens, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_Token[]
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokens` | **\HTMLPurifier_Token[]** | Array of HTMLPurifier_Token objects to be operated on. |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

Processed array of token objects.




***


***
> Automatically generated on 2025-03-18
