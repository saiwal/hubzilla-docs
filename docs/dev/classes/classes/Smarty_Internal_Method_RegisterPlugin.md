***

# Smarty_Internal_Method_RegisterPlugin

Smarty Method RegisterPlugin

Smarty::registerPlugin() method

* Full name: `\Smarty_Internal_Method_RegisterPlugin`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerPlugin

Registers plugin to be used in templates

```php
public registerPlugin(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $type, string $name, callable $callback, bool $cacheable = true, mixed $cache_attr = null): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$type` | **string** | plugin type |
| `$name` | **string** | name of template tag |
| `$callback` | **callable** | PHP callback to register |
| `$cacheable` | **bool** | if true (default) this<br />function is cache able |
| `$cache_attr` | **mixed** | caching attributes if any |




**Throws:**
<p>when the plugin tag is invalid</p>

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.plugin.tpl - 

***


***
> Automatically generated on 2025-03-15
