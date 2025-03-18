
# HTMLPurifier_AttrDef_Switch

Decorator that, depending on a token, switches between two definitions.



* Full name: `\HTMLPurifier_AttrDef_Switch`



## Properties


### tag



```php
protected $tag
```






***

### withTag



```php
protected $withTag
```






***

### withoutTag



```php
protected $withoutTag
```






***

## Methods


### __construct



```php
public __construct(string $tag, \HTMLPurifier_AttrDef $with_tag, \HTMLPurifier_AttrDef $without_tag): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | Tag name to switch upon |
| `$with_tag` | **\HTMLPurifier_AttrDef** | Call if token matches tag |
| `$without_tag` | **\HTMLPurifier_AttrDef** | Call if token doesn&#039;t match, or there is no token |





***

### validate



```php
public validate(string $string, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


***
> Automatically generated on 2025-03-18
