
# Smarty_Internal_Config_File_Compiler

Main config file compiler class



* Full name: `\Smarty_Internal_Config_File_Compiler`



## Properties


### lexer_class

Lexer class name

```php
public string $lexer_class
```






***

### parser_class

Parser class name

```php
public string $parser_class
```






***

### lex

Lexer object

```php
public object $lex
```






***

### parser

Parser object

```php
public object $parser
```






***

### smarty

Smarty object

```php
public \Smarty $smarty
```






***

### template

Smarty object

```php
public \Smarty_Internal_Template $template
```






***

### config_data

Compiled config data sections and variables

```php
public array $config_data
```






***

### write_compiled_code

compiled config data must always be written

```php
public bool $write_compiled_code
```






***

## Methods


### __construct

Initialize compiler

```php
public __construct(string $lexer_class, string $parser_class, \Smarty $smarty): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lexer_class` | **string** | class name |
| `$parser_class` | **string** | class name |
| `$smarty` | **\Smarty** | global instance |





***

### compileTemplate

Method to compile Smarty config source.

```php
public compileTemplate(\Smarty_Internal_Template $template): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |


**Return Value:**

true if compiling succeeded, false if it failed



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### trigger_config_file_error

display compiler error messages without dying
If parameter $args is empty it is a parser detected syntax error.

```php
public trigger_config_file_error(string $args = null): mixed
```

In this case the parser is called to obtain information about expected tokens.
If parameter $args contains a string this is used as error message






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **string** | individual error message or null |




**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***


***
> Automatically generated on 2025-03-18
