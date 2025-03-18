
# Smarty_Internal_Method_ConfigLoad

Smarty Method ConfigLoad

Smarty::configLoad() method

* Full name: `\Smarty_Internal_Method_ConfigLoad`



## Properties


### objMap

Valid for all objects

```php
public int $objMap
```






***

## Methods


### configLoad

load a config file, optionally load just selected sections

```php
public configLoad(\Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $data, string $config_file, mixed $sections = null): \Smarty|\Smarty_Internal_Data|\Smarty_Internal_Template
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$config_file` | **string** | filename |
| `$sections` | **mixed** | array of section names, single<br />section or null |




**Throws:**

- [`Exception`](./Exception.md)



**See Also:**

* https://www.smarty.net/docs/en/api.config.load.tpl - 

***

### _loadConfigFile

load a config file, optionally load just selected sections

```php
public _loadConfigFile(\Smarty|\Smarty_Internal_Data|\Smarty_Internal_Template $data, string $config_file, mixed $sections = null, int $scope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty&#124;\Smarty_Internal_Data&#124;\Smarty_Internal_Template** |  |
| `$config_file` | **string** | filename |
| `$sections` | **mixed** | array of section names, single<br />section or null |
| `$scope` | **int** | scope into which config variables<br />shall be loaded |




**Throws:**

- [`Exception`](./Exception.md)



**See Also:**

* https://www.smarty.net/docs/en/api.config.load.tpl - 

***

### _loadConfigVars

load config variables into template object

```php
public _loadConfigVars(\Smarty_Internal_Template $tpl, array $new_config_vars): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$new_config_vars` | **array** |  |





***

### _assignConfigVars

Assign all config variables in given scope

```php
public _assignConfigVars(array& $config_vars, \Smarty_Internal_Template $tpl, array $new_config_vars): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config_vars` | **array** | config variables in scope |
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$new_config_vars` | **array** | loaded config variables |





***

### _updateVarStack

Update config variables in template local variable stack

```php
public _updateVarStack(\Smarty_Internal_Template $tpl, array $config_vars): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$config_vars` | **array** |  |





***

### _getConfigVariable

gets  a config variable value

```php
public _getConfigVariable(\Smarty|\Smarty_Internal_Data|\Smarty_Internal_Template $data, string $varName, bool $errorEnable = true): null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty&#124;\Smarty_Internal_Data&#124;\Smarty_Internal_Template** |  |
| `$varName` | **string** | the name of the config variable |
| `$errorEnable` | **bool** |  |


**Return Value:**

the value of the config variable




***


***
> Automatically generated on 2025-03-18
