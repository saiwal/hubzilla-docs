
# Smarty_Internal_Method_RegisterDefaultPluginHandler

Smarty Method RegisterDefaultPluginHandler

Smarty::registerDefaultPluginHandler() method

* Full name: `\Smarty_Internal_Method_RegisterDefaultPluginHandler`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerDefaultPluginHandler

Registers a default plugin handler

```php
public registerDefaultPluginHandler(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, callable $callback): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$callback` | **callable** | class/method name |




**Throws:**
<p>if $callback is not callable</p>

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.default.plugin.handler.tpl - 

***


***
> Automatically generated on 2025-03-15
