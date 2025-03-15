***

# HTMLPurifier_Strategy_Composite

Composite strategy that runs multiple strategies on tokens.



* Full name: `\HTMLPurifier_Strategy_Composite`
* Parent class: [`\HTMLPurifier_Strategy`](./HTMLPurifier_Strategy.md)
* This class is an **Abstract class**



## Properties


### strategies

List of strategies to run tokens through.

```php
protected $strategies
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
