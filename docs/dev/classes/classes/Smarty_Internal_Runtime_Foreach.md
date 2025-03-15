
# Smarty_Internal_Runtime_Foreach

Foreach Runtime Methods count(), init(), restore()



* Full name: `\Smarty_Internal_Runtime_Foreach`



## Properties


### stack

Stack of saved variables

```php
private array $stack
```






***

## Methods


### init

Init foreach loop
 - save item and key variables, named foreach property data if defined
 - init item and key variables, named foreach property data if required
 - count total if required

```php
public init(\Smarty_Internal_Template $tpl, mixed $from, string $item, bool $needTotal = false, null|string $key = null, null|string $name = null, array $properties = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$from` | **mixed** | values to loop over |
| `$item` | **string** | variable name |
| `$needTotal` | **bool** | flag if we need to count values |
| `$key` | **null&#124;string** | variable name |
| `$name` | **null&#124;string** | of named foreach |
| `$properties` | **array** | of named foreach |


**Return Value:**

$from




***

### count

[util function] counts an array, arrayAccess/traversable or PDOStatement object

```php
public count(mixed $value): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |


**Return Value:**

the count for arrays and objects that implement countable, 1 for other objects that don't, and 0
for empty elements




***

### restore

Restore saved variables

```php
public restore(\Smarty_Internal_Template $tpl, int $levels = 1): mixed
```

will be called by {break n} or {continue n} for the required number of levels






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$levels` | **int** | number of levels |





***


***
> Automatically generated on 2025-03-15
