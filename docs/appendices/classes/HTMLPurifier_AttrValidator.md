
# HTMLPurifier_AttrValidator

Validates the attributes of a token. Doesn't manage required attributes
very well. The only reason we factored this out was because RemoveForeignElements
also needed it besides ValidateAttributes.



* Full name: `\HTMLPurifier_AttrValidator`




## Methods


### validateToken

Validates the attributes of a token, mutating it as necessary.

```php
public validateToken(\HTMLPurifier_Token $token, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): mixed
```

that has valid tokens






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **\HTMLPurifier_Token** | Token to validate. |
| `$config` | **\HTMLPurifier_Config** | Instance of HTMLPurifier_Config |
| `$context` | **\HTMLPurifier_Context** | Instance of HTMLPurifier_Context |





***


***
> Automatically generated on 2025-03-18
