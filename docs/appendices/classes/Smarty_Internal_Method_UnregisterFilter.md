
# Smarty_Internal_Method_UnregisterFilter

Smarty Method UnregisterFilter

Smarty::unregisterFilter() method

* Full name: `\Smarty_Internal_Method_UnregisterFilter`
* Parent class: [`\Smarty_Internal_Method_RegisterFilter`](./Smarty_Internal_Method_RegisterFilter.md)




## Methods


### unregisterFilter

Unregisters a filter function

```php
public unregisterFilter(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $type, callable|string $callback): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$type` | **string** | filter type |
| `$callback` | **callable&#124;string** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.unregister.filter.tpl - 

***


## Inherited methods


### registerFilter

Registers a filter function

```php
public registerFilter(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $type, callable $callback, string|null $name = null): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$type` | **string** | filter type |
| `$callback` | **callable** |  |
| `$name` | **string&#124;null** | optional filter name |




**Throws:**

- [`SmartyException`](./SmartyException.md)



**See Also:**

* https://www.smarty.net/docs/en/api.register.filter.tpl - 

***

### _getFilterName

Return internal filter name

```php
public _getFilterName(callable $function_name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$function_name` | **callable** |  |


**Return Value:**

internal filter name




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
> Automatically generated on 2025-03-18
