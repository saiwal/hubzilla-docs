***

# Smarty_Internal_Method_MustCompile

Smarty Method MustCompile

Smarty_Internal_Template::mustCompile() method

* Full name: `\Smarty_Internal_Method_MustCompile`



## Properties


### objMap

Valid for template object

```php
public int $objMap
```






***

## Methods


### mustCompile

Returns if the current template must be compiled by the Smarty compiler
It does compare the timestamps of template source and the compiled templates and checks the force compile
configuration

```php
public mustCompile(\Smarty_Internal_Template $_template): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
