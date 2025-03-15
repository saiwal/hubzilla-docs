***

# Smarty_Internal_Method_UnloadFilter

Smarty Method UnloadFilter

Smarty::unloadFilter() method

* Full name: `\Smarty_Internal_Method_UnloadFilter`
* Parent class: [`\Smarty_Internal_Method_LoadFilter`](./Smarty_Internal_Method_LoadFilter.md)




## Methods


### unloadFilter

load a filter of specified type and name

```php
public unloadFilter(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $type, string $name): \Smarty_Internal_TemplateBase
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$type` | **string** | filter type |
| `$name` | **string** | filter name |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.unload.filter.tpl - 

***


## Inherited methods


### loadFilter

load a filter of specified type and name

```php
public loadFilter(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $type, string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$type` | **string** | filter type |
| `$name` | **string** | filter name |




**Throws:**
<p>if filter could not be loaded</p>

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.load.filter.tpl - 

***

### _checkFilterType

Check if filter type is valid

```php
public _checkFilterType(string $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
