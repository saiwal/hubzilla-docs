
# Smarty_Internal_Method_GetAutoloadFilters

Smarty Method GetAutoloadFilters

Smarty::getAutoloadFilters() method

* Full name: `\Smarty_Internal_Method_GetAutoloadFilters`
* Parent class: [`\Smarty_Internal_Method_SetAutoloadFilters`](./Smarty_Internal_Method_SetAutoloadFilters.md)




## Methods


### getAutoloadFilters

Get autoload filters

```php
public getAutoloadFilters(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, string $type = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$type` | **string** | type of filter to get auto loads<br />for. Defaults to all autoload<br />filters |


**Return Value:**

array( 'type1' => array( 'filter1', 'filter2', … ) ) or array( 'filter1', 'filter2', …) if $type
was specified



**Throws:**

- [`SmartyException`](./SmartyException.md)



***


## Inherited methods


### setAutoloadFilters

Set autoload filters

```php
public setAutoloadFilters(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, array $filters, string $type = null): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$filters` | **array** | filters to load automatically |
| `$type` | **string** | &quot;pre&quot;, &quot;output&quot;, … specify<br />the filter type to set.<br />Defaults to none treating<br />$filters&#039; keys as the<br />appropriate types |




**Throws:**

- [`SmartyException`](./SmartyException.md)



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
