***

# Smarty_Internal_Runtime_TplFunction

TplFunction Runtime Methods callTemplateFunction



* Full name: `\Smarty_Internal_Runtime_TplFunction`




## Methods


### callTemplateFunction

Call template function

```php
public callTemplateFunction(\Smarty_Internal_Template $tpl, string $name, array $params, bool $nocache): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** | template object |
| `$name` | **string** | template function name |
| `$params` | **array** | parameter array |
| `$nocache` | **bool** | true if called nocache |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### registerTplFunctions

Register template functions defined by template

```php
public registerTplFunctions(\Smarty|\Smarty_Internal_Template|\Smarty_Internal_TemplateBase $obj, array $tplFunctions, bool $override = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty&#124;\Smarty_Internal_Template&#124;\Smarty_Internal_TemplateBase** |  |
| `$tplFunctions` | **array** | source information array of<br />template functions defined<br />in template |
| `$override` | **bool** | if true replace existing<br />functions with same name |





***

### getTplFunction

Return source parameter array for single or all template functions

```php
public getTplFunction(\Smarty_Internal_Template $tpl, null|string $name = null): array|bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** | template object |
| `$name` | **null&#124;string** | template function name |





***

### addTplFuncToCache

Add template function to cache file for nocache calls

```php
public addTplFuncToCache(\Smarty_Internal_Template $tpl, string $_name, string $_function): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$_name` | **string** | template function name |
| `$_function` | **string** | PHP function name |





***

### saveTemplateVariables

Save current template variables on stack

```php
public saveTemplateVariables(\Smarty_Internal_Template $tpl, string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$name` | **string** | stack name |





***

### restoreTemplateVariables

Restore saved variables into template objects

```php
public restoreTemplateVariables(\Smarty_Internal_Template $tpl, string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$name` | **string** | stack name |





***


***
> Automatically generated on 2025-03-15
