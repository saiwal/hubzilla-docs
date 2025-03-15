***

# Smarty_Internal_Method_RegisterObject

Smarty Method RegisterObject

Smarty::registerObject() method

* Full name: `\Smarty_Internal_Method_RegisterObject`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerObject

Registers object to be used in templates

```php
public registerObject(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $object_name, object $object, array $allowed_methods_properties = array(), bool $format = true, array $block_methods = array()): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$object_name` | **string** |  |
| `$object` | **object** | the<br />referenced<br />PHP<br />object<br />to<br />register |
| `$allowed_methods_properties` | **array** | list of<br />allowed<br />methods<br />(empty<br />= all) |
| `$format` | **bool** | smarty<br />argument<br />format,<br />else<br />traditional |
| `$block_methods` | **array** | list of<br />block-methods |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.object.tpl - 

***


***
> Automatically generated on 2025-03-15
