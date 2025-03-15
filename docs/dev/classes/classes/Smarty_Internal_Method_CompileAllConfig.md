
# Smarty_Internal_Method_CompileAllConfig

Smarty Method CompileAllConfig

Smarty::compileAllConfig() method

* Full name: `\Smarty_Internal_Method_CompileAllConfig`
* Parent class: [`\Smarty_Internal_Method_CompileAllTemplates`](./Smarty_Internal_Method_CompileAllTemplates.md)




## Methods


### compileAllConfig

Compile all config files

```php
public compileAllConfig(\Smarty $smarty, string $extension = &#039;.conf&#039;, bool $force_compile = false, int $time_limit, int $max_errors = null): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | passed smarty object |
| `$extension` | **string** | file extension |
| `$force_compile` | **bool** | force all to recompile |
| `$time_limit` | **int** |  |
| `$max_errors` | **int** |  |


**Return Value:**

number of template files recompiled




***


## Inherited methods


### compileAllTemplates

Compile all template files

```php
public compileAllTemplates(\Smarty $smarty, string $extension = &#039;.tpl&#039;, bool $force_compile = false, int $time_limit, int $max_errors = null): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | passed smarty object |
| `$extension` | **string** | file extension |
| `$force_compile` | **bool** | force all to recompile |
| `$time_limit` | **int** |  |
| `$max_errors` | **int** |  |


**Return Value:**

number of template files recompiled




***

### compileAll

Compile all template or config files

```php
protected compileAll(\Smarty $smarty, string $extension, bool $force_compile, int $time_limit, int $max_errors, bool $isConfig = false): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$extension` | **string** | template file name extension |
| `$force_compile` | **bool** | force all to recompile |
| `$time_limit` | **int** | set maximum execution time |
| `$max_errors` | **int** | set maximum allowed errors |
| `$isConfig` | **bool** | flag true if called for config files |


**Return Value:**

number of template files compiled




***


***
> Automatically generated on 2025-03-15
