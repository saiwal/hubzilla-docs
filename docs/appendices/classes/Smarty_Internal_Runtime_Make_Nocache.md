
# Smarty_Internal_Runtime_Make_Nocache

{make_nocache} Runtime Methods save(), store()



* Full name: `\Smarty_Internal_Runtime_Make_Nocache`




## Methods


### save

Save current variable value while rendering compiled template and inject nocache code to
assign variable value in cahed template

```php
public save(\Smarty_Internal_Template $tpl, string $var): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$var` | **string** | variable name |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### store

Store variable value saved while rendering compiled template in cached template context

```php
public store(\Smarty_Internal_Template $tpl, string $var, array $properties): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$var` | **string** | variable name |
| `$properties` | **array** |  |





***


***
> Automatically generated on 2025-03-18
