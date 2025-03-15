
# Smarty_Internal_Runtime_Capture

Runtime Extension Capture



* Full name: `\Smarty_Internal_Runtime_Capture`



## Properties


### isPrivateExtension

Flag that this instance  will not be cached

```php
public bool $isPrivateExtension
```






***

### captureStack

Stack of capture parameter

```php
private array $captureStack
```






***

### captureCount

Current open capture sections

```php
private int $captureCount
```






***

### countStack

Count stack

```php
private int[] $countStack
```






***

### namedBuffer

Named buffer

```php
private string[] $namedBuffer
```






***

### isRegistered

Flag if callbacks are registered

```php
private bool $isRegistered
```






***

## Methods


### open

Open capture section

```php
public open(\Smarty_Internal_Template $_template, string $buffer, string $assign, string $append): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |
| `$buffer` | **string** | capture name |
| `$assign` | **string** | variable name |
| `$append` | **string** | variable name |





***

### register

Register callbacks in template class

```php
private register(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |





***

### startRender

Start render callback

```php
public startRender(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |





***

### close

Close capture section

```php
public close(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### error

Error exception on not matching {capture}{/capture}

```php
public error(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### getBuffer

Return content of named capture buffer by key or as array

```php
public getBuffer(\Smarty_Internal_Template $_template, string|null $name = null): string|string[]|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |
| `$name` | **string&#124;null** |  |





***

### endRender

End render callback

```php
public endRender(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
