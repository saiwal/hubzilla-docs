
# Smarty_Template_Compiled

Smarty Resource Data Object
Meta Data Container for Template Files



* Full name: `\Smarty_Template_Compiled`
* Parent class: [`\Smarty_Template_Resource_Base`](./Smarty_Template_Resource_Base.md)



## Properties


### nocache_hash

nocache hash

```php
public string|null $nocache_hash
```






***

## Methods


### load

get a Compiled Object of this source

```php
public static load(\Smarty_Internal_Template $_template): \Smarty_Template_Compiled
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |


**Return Value:**

compiled object




***

### populateCompiledFilepath

populate Compiled Object with compiled filepath

```php
public populateCompiledFilepath(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |





***

### render

render compiled template code

```php
public render(\Smarty_Internal_Template $_template): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### process

load compiled template or compile from source

```php
public process(\Smarty_Internal_Template $_smarty_tpl): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_smarty_tpl` | **\Smarty_Internal_Template** | do not change variable name, is used by compiled template |




**Throws:**

- [`Exception`](./Exception.md)



***

### compileTemplateSource

compile template from source

```php
public compileTemplateSource(\Smarty_Internal_Template $_template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### write

Write compiled code by handler

```php
public write(\Smarty_Internal_Template $_template, string $code): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |
| `$code` | **string** | compiled code |


**Return Value:**

success



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### read

Read compiled content from handler

```php
public read(\Smarty_Internal_Template $_template): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |


**Return Value:**

content




***

### loadCompiledTemplate

Load fresh compiled template by including the PHP file
HHVM requires a work around because of a PHP incompatibility

```php
private loadCompiledTemplate(\Smarty_Internal_Template $_smarty_tpl): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_smarty_tpl` | **\Smarty_Internal_Template** | do not change variable name, is used by compiled template |





***


## Inherited methods


### process

Process resource

```php
public process(\Smarty_Internal_Template $_template): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |





***

### getRenderedTemplateCode

get rendered template content by calling compiled or cached template code

```php
public getRenderedTemplateCode(\Smarty_Internal_Template $_template, string $unifunc = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** |  |
| `$unifunc` | **string** | function with template code |




**Throws:**

- [`Exception`](./Exception.md)



***

### getTimeStamp

Get compiled time stamp

```php
public getTimeStamp(): int
```












***


***
> Automatically generated on 2025-03-15
