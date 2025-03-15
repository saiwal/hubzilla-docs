
# Smarty_Internal_Method_RegisterDefaultTemplateHandler

Smarty Method RegisterDefaultTemplateHandler

Smarty::registerDefaultTemplateHandler() method

* Full name: `\Smarty_Internal_Method_RegisterDefaultTemplateHandler`



## Properties


### objMap

Valid for Smarty and template object

```php
public int $objMap
```






***

## Methods


### registerDefaultTemplateHandler

Register template default handler

```php
public registerDefaultTemplateHandler(\Smarty_Internal_TemplateBase|\Smarty_Internal_Template|\Smarty $obj, callable $callback): \Smarty|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_TemplateBase&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$callback` | **callable** | class/method name |




**Throws:**
<p>if $callback is not callable</p>

- [`SmartyException`](./SmartyException.md)



***

### _getDefaultTemplate

get default content from template or config resource handler

```php
public static _getDefaultTemplate(\Smarty_Template_Source $source): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Smarty_Template_Source** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
