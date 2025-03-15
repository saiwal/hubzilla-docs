***

# Smarty_Internal_Runtime_Inheritance

Inheritance Runtime Methods processBlock, endChild, init



* Full name: `\Smarty_Internal_Runtime_Inheritance`



## Properties


### state

State machine
- 0 idle next extends will create a new inheritance tree
- 1 processing child template
- 2 wait for next inheritance template
- 3 assume parent template, if child will loaded goto state 1
    a call to a sub template resets the state to 0

```php
public int $state
```






***

### childRoot

Array of root child {block} objects

```php
public \Smarty_Internal_Block[] $childRoot
```






***

### inheritanceLevel

inheritance template nesting level

```php
public int $inheritanceLevel
```






***

### tplIndex

inheritance template index

```php
public int $tplIndex
```






***

### sources

Array of template source objects

```php
public \Smarty_Template_Source[] $sources
```






***

### sourceStack

Stack of source objects while executing block code

```php
public \Smarty_Template_Source[] $sourceStack
```






***

## Methods


### init

Initialize inheritance

```php
public init(\Smarty_Internal_Template $tpl, bool $initChild, array $blockNames = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** | template object of caller |
| `$initChild` | **bool** | if true init for child template |
| `$blockNames` | **array** | outer level block name |





***

### endChild

End of child template(s)
- if outer level is reached flush output buffer and switch to wait for parent template state

```php
public endChild(\Smarty_Internal_Template $tpl, null|string $template = null, null|string $uid = null, null|string $func = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$template` | **null&#124;string** | optional name of inheritance parent template |
| `$uid` | **null&#124;string** | uid of inline template |
| `$func` | **null&#124;string** | function call name of inline template |




**Throws:**

- [`Exception`](./Exception.md)

- [`SmartyException`](./SmartyException.md)



***

### instanceBlock

Smarty_Internal_Block constructor.

```php
public instanceBlock(\Smarty_Internal_Template $tpl, mixed $className, string $name, int|null $tplIndex = null): mixed
```

- if outer level {block} of child template ($state === 1) save it as child root block
- otherwise process inheritance and render






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$className` | **mixed** |  |
| `$name` | **string** |  |
| `$tplIndex` | **int&#124;null** | index of outer level {block} if nested |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### process

Goto child block or render this

```php
public process(\Smarty_Internal_Template $tpl, \Smarty_Internal_Block $block, \Smarty_Internal_Block|null $parent = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$block` | **\Smarty_Internal_Block** |  |
| `$parent` | **\Smarty_Internal_Block&#124;null** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### callChild

Render child on \$smarty.block.child

```php
public callChild(\Smarty_Internal_Template $tpl, \Smarty_Internal_Block $block): null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$block` | **\Smarty_Internal_Block** |  |


**Return Value:**

block content



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### callParent

Render parent block on \$smarty.block.parent or {block append/prepend}

```php
public callParent(\Smarty_Internal_Template $tpl, \Smarty_Internal_Block $block, string $tag): null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |
| `$block` | **\Smarty_Internal_Block** |  |
| `$tag` | **string** |  |


**Return Value:**

block content



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### callBlock

render block

```php
public callBlock(\Smarty_Internal_Block $block, \Smarty_Internal_Template $tpl): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\Smarty_Internal_Block** |  |
| `$tpl` | **\Smarty_Internal_Template** |  |





***


***
> Automatically generated on 2025-03-15
