***

# Smarty_Internal_Method_AddAutoloadFilters

Smarty Method AddAutoloadFilters

Smarty::addAutoloadFilters() method

* Full name: `\Smarty_Internal_Method_AddAutoloadFilters`
* Parent class: [`\Smarty_Internal_Method_SetAutoloadFilters`](./Smarty_Internal_Method_SetAutoloadFilters.md)




## Methods


### addAutoloadFilters

Add autoload filters

```php
public addAutoloadFilters(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, array $filters, string $type = null): \Smarty|\Smarty_Internal_Template
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
