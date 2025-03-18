
# Smarty_Variable

class for the Smarty variable object
This class defines the Smarty variable object



* Full name: `\Smarty_Variable`



## Properties


### value

template variable

```php
public mixed $value
```






***

### nocache

if true any output of this variable will be not cached

```php
public bool $nocache
```






***

## Methods


### __construct

create Smarty variable object

```php
public __construct(mixed $value = null, bool $nocache = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** | the value to assign |
| `$nocache` | **bool** | if true any output of this variable will be not cached |





***

### __toString

<<magic>> String conversion

```php
public __toString(): string
```












***


***
> Automatically generated on 2025-03-18
