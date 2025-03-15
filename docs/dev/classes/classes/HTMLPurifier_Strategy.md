***

# HTMLPurifier_Strategy

Supertype for classes that define a strategy for modifying/purifying tokens.

While HTMLPurifier's core purpose is fixing HTML into something proper,
strategies provide plug points for extra configuration or even extra
features, such as custom tags, custom parsing of text, etc.

* Full name: `\HTMLPurifier_Strategy`
* This class is an **Abstract class**




## Methods


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
