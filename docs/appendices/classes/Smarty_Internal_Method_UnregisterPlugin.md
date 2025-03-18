
# Smarty_Internal_Method_UnregisterPlugin

Smarty Method UnregisterPlugin

Smarty::unregisterPlugin() method

* Full name: `\Smarty_Internal_Method_UnregisterPlugin`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### unregisterPlugin

Registers plugin to be used in templates

```php
public unregisterPlugin(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $type, string $name): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$type` | **string** | plugin type |
| `$name` | **string** | name of template tag |





**See Also:**

* https://www.smarty.net/docs/en/api.unregister.plugin.tpl - 

***


***
> Automatically generated on 2025-03-18
