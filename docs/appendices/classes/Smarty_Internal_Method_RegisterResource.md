
# Smarty_Internal_Method_RegisterResource

Smarty Method RegisterResource

Smarty::registerResource() method

* Full name: `\Smarty_Internal_Method_RegisterResource`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerResource

Registers a resource to fetch a template

```php
public registerResource(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $name, \Smarty_Resource $resource_handler): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$name` | **string** | name of resource type |
| `$resource_handler` | **\Smarty_Resource** | instance of Smarty_Resource |





**See Also:**

* https://www.smarty.net/docs/en/api.register.resource.tpl - 

***


***
> Automatically generated on 2025-03-18
