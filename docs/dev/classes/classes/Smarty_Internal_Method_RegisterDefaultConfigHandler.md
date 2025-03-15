***

# Smarty_Internal_Method_RegisterDefaultConfigHandler

Smarty Method RegisterDefaultConfigHandler

Smarty::registerDefaultConfigHandler() method

* Full name: `\Smarty_Internal_Method_RegisterDefaultConfigHandler`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerDefaultConfigHandler

Register config default handler

```php
public registerDefaultConfigHandler(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, callable $callback): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$callback` | **callable** | class/method name |




**Throws:**
<p>if $callback is not callable</p>

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
