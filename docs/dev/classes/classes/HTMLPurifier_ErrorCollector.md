
# HTMLPurifier_ErrorCollector

Error collection class that enables HTML Purifier to report HTML
problems back to the user



* Full name: `\HTMLPurifier_ErrorCollector`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`LINENO`|public| |0|
|`SEVERITY`|public| |1|
|`MESSAGE`|public| |2|
|`CHILDREN`|public| |3|

## Properties


### errors



```php
protected $errors
```






***

### _current



```php
protected $_current
```






***

### _stacks



```php
protected $_stacks
```






***

### locale



```php
protected $locale
```






***

### generator



```php
protected $generator
```






***

### context



```php
protected $context
```






***

### lines



```php
protected $lines
```






***

## Methods


### __construct



```php
public __construct(\HTMLPurifier_Context $context): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$context` | **\HTMLPurifier_Context** |  |





***

### send

Sends an error message to the collector for later use

```php
public send(int $severity, string $msg): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$severity` | **int** | Error severity, PHP error style (don&#039;t use E_USER_) |
| `$msg` | **string** | Error message text |





***

### getRaw

Retrieves raw error data for custom formatter to use

```php
public getRaw(): mixed
```












***

### getHTMLFormatted

Default HTML formatting implementation for error messages

```php
public getHTMLFormatted(\HTMLPurifier_Config $config, array $errors = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** | Configuration, vital for HTML output nature |
| `$errors` | **array** | Errors array to display; used for recursion. |





***

### _renderStruct



```php
private _renderStruct(mixed& $ret, mixed $struct, mixed $line = null, mixed $col = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ret` | **mixed** |  |
| `$struct` | **mixed** |  |
| `$line` | **mixed** |  |
| `$col` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
