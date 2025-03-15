***

# Smarty_Internal_Block

Smarty {block} tag class



* Full name: `\Smarty_Internal_Block`



## Properties


### name

Block name

```php
public string $name
```






***

### hide

Hide attribute

```php
public bool $hide
```






***

### append

Append attribute

```php
public bool $append
```






***

### prepend

prepend attribute

```php
public bool $prepend
```






***

### callsChild

Block calls $smarty.block.child

```php
public bool $callsChild
```






***

### child

Inheritance child block

```php
public \Smarty_Internal_Block|null $child
```






***

### parent

Inheritance calling parent block

```php
public \Smarty_Internal_Block|null $parent
```






***

### tplIndex

Inheritance Template index

```php
public int $tplIndex
```






***

## Methods


### __construct

Smarty_Internal_Block constructor.

```php
public __construct(string $name, int|null $tplIndex): mixed
```

- if outer level {block} of child template ($state === 1) save it as child root block
- otherwise process inheritance and render






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | block name |
| `$tplIndex` | **int&#124;null** | index of outer level {block} if nested |





***

### callBlock

Compiled block code overloaded by {block} class

```php
public callBlock(\Smarty_Internal_Template $tpl): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tpl` | **\Smarty_Internal_Template** |  |





***


***
> Automatically generated on 2025-03-15
