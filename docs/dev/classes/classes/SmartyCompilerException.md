***

# SmartyCompilerException

Smarty compiler exception class



* Full name: `\SmartyCompilerException`
* Parent class: [`\SmartyException`](./SmartyException.md)



## Properties


### source

The template source snippet relating to the error

```php
public $source
```






***

### desc

The raw text of the error message

```php
public $desc
```






***

### template

The resource identifier or template name

```php
public $template
```






***

## Methods


### __construct

The constructor of the exception

```php
public __construct(string $message = &quot;&quot;, int $code, string|null $filename = null, int|null $line = null, \Throwable|null $previous = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** | The Exception message to throw. |
| `$code` | **int** | The Exception code. |
| `$filename` | **string&#124;null** | The filename where the exception is thrown. |
| `$line` | **int&#124;null** | The line number where the exception is thrown. |
| `$previous` | **\Throwable&#124;null** | The previous exception used for the exception chaining. |





***

### __toString



```php
public __toString(): string
```












***

### setLine



```php
public setLine(int $line): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **int** |  |





***


## Inherited methods


### __toString



```php
public __toString(): string
```












***


***
> Automatically generated on 2025-03-15
