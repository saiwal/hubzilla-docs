***

# Smarty_Internal_Method_GetRegisteredObject

Smarty Method GetRegisteredObject

Smarty::getRegisteredObject() method

* Full name: `\Smarty_Internal_Method_GetRegisteredObject`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### getRegisteredObject

return a reference to a registered object

```php
public getRegisteredObject(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $object_name): object
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$object_name` | **string** | object name |




**Throws:**
<p>if no such object is found</p>

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.get.registered.object.tpl - 

***


***
> Automatically generated on 2025-03-15
