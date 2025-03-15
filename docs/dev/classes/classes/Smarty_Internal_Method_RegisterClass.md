***

# Smarty_Internal_Method_RegisterClass

Smarty Method RegisterClass

Smarty::registerClass() method

* Full name: `\Smarty_Internal_Method_RegisterClass`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerClass

Registers static classes to be used in templates

```php
public registerClass(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $class_name, string $class_impl): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$class_name` | **string** |  |
| `$class_impl` | **string** | the referenced PHP class to<br />register |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.class.tpl - 

***


***
> Automatically generated on 2025-03-15
