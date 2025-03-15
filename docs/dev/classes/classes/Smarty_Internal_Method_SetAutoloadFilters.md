***

# Smarty_Internal_Method_SetAutoloadFilters

Smarty Method SetAutoloadFilters

Smarty::setAutoloadFilters() method

* Full name: `\Smarty_Internal_Method_SetAutoloadFilters`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

### filterTypes

Valid filter types

```php
private array $filterTypes
```






***

## Methods


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
