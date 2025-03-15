***

# HTMLPurifier_Strategy_RemoveForeignElements

Removes all unrecognized tags from the list of tokens.

This strategy iterates through all the tokens and removes unrecognized
tokens. If a token is not recognized but a TagTransform is defined for
that element, the element will be transformed accordingly.

* Full name: `\HTMLPurifier_Strategy_RemoveForeignElements`
* Parent class: [`\HTMLPurifier_Strategy`](./HTMLPurifier_Strategy.md)




## Methods


### execute

Executes the strategy on the tokens.

```php
public execute(\HTMLPurifier_Token[] $tokens, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): array|\HTMLPurifier_Token[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokens` | **\HTMLPurifier_Token[]** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





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
> Automatically generated on 2025-03-15
