
# HTMLPurifier_Strategy_FixNesting

Takes a well formed list of tokens and fixes their nesting.

HTML elements dictate which elements are allowed to be their children,
for example, you can't have a p tag in a span tag.  Other elements have
much more rigorous definitions: tables, for instance, require a specific
order for their elements.  There are also constraints not expressible by
document type definitions, such as the chameleon nature of ins/del
tags and global child exclusions.

The first major objective of this strategy is to iterate through all
the nodes and determine whether or not their children conform to the
element's definition.  If they do not, the child definition may
optionally supply an amended list of elements that is valid or
require that the entire node be deleted (and the previous node
rescanned).

The second objective is to ensure that explicitly excluded elements of
an element do not appear in its children.  Code that accomplishes this
task is pervasive through the strategy, though the two are distinct tasks
and could, theoretically, be seperated (although it's not recommended).

* Full name: `\HTMLPurifier_Strategy_FixNesting`
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
