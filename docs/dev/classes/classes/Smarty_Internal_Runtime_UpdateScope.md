***

# Smarty_Internal_Runtime_UpdateScope

Runtime Extension updateScope



* Full name: `\Smarty_Internal_Runtime_UpdateScope`




## Methods


### _updateScope

Update new assigned template or config variable in other effected scopes

```php
public _updateScope(\Smarty_Internal_Template $tpl, string|null $varName, int $tagScope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** | data object |
| `$varName` | **string&#124;null** | variable name |
| `$tagScope` | **int** | tag scope to which bubble up variable value |





***

### _getAffectedScopes

Get array of objects which needs to be updated  by given scope value

```php
public _getAffectedScopes(\Smarty_Internal_Template $tpl, int $mergedScope): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$mergedScope` | **int** | merged tag and template scope to which bubble up variable value |





***

### _updateVariableInOtherScope

Update variable in other scope

```php
public _updateVariableInOtherScope(array& $tpl_vars, \Smarty_Internal_Template $from, string $varName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl_vars` | **array** | template variable array |
| `$from` | **\Smarty_Internal_Template** |  |
| `$varName` | **string** | variable name |





***

### _updateVarStack

Update variable in template local variable stack

```php
public _updateVarStack(\Smarty_Internal_Template $tpl, string|null $varName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$varName` | **string&#124;null** | variable name or null for config variables |





***


***
> Automatically generated on 2025-03-15
