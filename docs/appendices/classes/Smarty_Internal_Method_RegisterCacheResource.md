
# Smarty_Internal_Method_RegisterCacheResource

Smarty Method RegisterCacheResource

Smarty::registerCacheResource() method

* Full name: `\Smarty_Internal_Method_RegisterCacheResource`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerCacheResource

Registers a resource to fetch a template

```php
public registerCacheResource(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $name, \Smarty_CacheResource $resource_handler): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$name` | **string** | name of resource type |
| `$resource_handler` | **\Smarty_CacheResource** |  |





**See Also:**

* https://www.smarty.net/docs/en/api.register.cacheresource.tpl - 

***


***
> Automatically generated on 2025-03-18
