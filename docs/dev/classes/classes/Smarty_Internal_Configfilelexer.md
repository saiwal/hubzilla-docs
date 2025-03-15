
# Smarty_Internal_Configfilelexer

Smarty_Internal_Configfilelexer

This is the config file lexer.
It is generated from the smarty_internal_configfilelexer.plex file

* Full name: `\Smarty_Internal_Configfilelexer`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`START`|public| |1|
|`VALUE`|public| |2|
|`NAKED_STRING_VALUE`|public| |3|
|`COMMENT`|public| |4|
|`SECTION`|public| |5|
|`TRIPPLE`|public| |6|

## Properties


### data

Source

```php
public string $data
```






***

### dataLength

Source length

```php
public int $dataLength
```






***

### counter

byte counter

```php
public int $counter
```






***

### token

token number

```php
public int $token
```






***

### value

token value

```php
public string $value
```






***

### line

current line

```php
public int $line
```






***

### state

state number

```php
public int $state
```






***

### smarty

Smarty object

```php
public \Smarty $smarty
```






***

### yyTraceFILE

trace file

```php
public resource $yyTraceFILE
```






***

### yyTracePrompt

trace prompt

```php
public string $yyTracePrompt
```






***

### state_name

state names

```php
public array $state_name
```






***

### smarty_token_names

token names

```php
public array $smarty_token_names
```






***

### compiler

compiler object

```php
private \Smarty_Internal_Config_File_Compiler $compiler
```






***

### configBooleanize

copy of config_booleanize

```php
private bool $configBooleanize
```






***

### yy_global_pattern1

storage for assembled token patterns

```php
private string $yy_global_pattern1
```






***

### yy_global_pattern2



```php
private $yy_global_pattern2
```






***

### yy_global_pattern3



```php
private $yy_global_pattern3
```






***

### yy_global_pattern4



```php
private $yy_global_pattern4
```






***

### yy_global_pattern5



```php
private $yy_global_pattern5
```






***

### yy_global_pattern6



```php
private $yy_global_pattern6
```






***

### _yy_state



```php
private $_yy_state
```






***

### _yy_stack



```php
private $_yy_stack
```






***

## Methods


### __construct

constructor

```php
public __construct(string $data, \Smarty_Internal_Config_File_Compiler $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | template source |
| `$compiler` | **\Smarty_Internal_Config_File_Compiler** |  |





***

### replace



```php
public replace(mixed $input): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***

### PrintTrace



```php
public PrintTrace(): mixed
```












***

### yylex



```php
public yylex(): mixed
```












***

### yypushstate



```php
public yypushstate(mixed $state): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$state` | **mixed** |  |





***

### yypopstate



```php
public yypopstate(): mixed
```












***

### yybegin



```php
public yybegin(mixed $state): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$state` | **mixed** |  |





***

### yylex1



```php
public yylex1(): mixed
```












***

### yy_r1_1



```php
public yy_r1_1(): mixed
```












***

### yy_r1_2



```php
public yy_r1_2(): mixed
```












***

### yy_r1_3



```php
public yy_r1_3(): mixed
```












***

### yy_r1_4



```php
public yy_r1_4(): mixed
```












***

### yy_r1_5



```php
public yy_r1_5(): mixed
```












***

### yy_r1_6



```php
public yy_r1_6(): mixed
```












***

### yy_r1_7



```php
public yy_r1_7(): mixed
```












***

### yy_r1_8



```php
public yy_r1_8(): mixed
```












***

### yylex2



```php
public yylex2(): mixed
```












***

### yy_r2_1



```php
public yy_r2_1(): mixed
```












***

### yy_r2_2



```php
public yy_r2_2(): mixed
```












***

### yy_r2_3



```php
public yy_r2_3(): mixed
```












***

### yy_r2_4



```php
public yy_r2_4(): mixed
```












***

### yy_r2_5



```php
public yy_r2_5(): mixed
```












***

### yy_r2_6



```php
public yy_r2_6(): mixed
```












***

### yy_r2_7



```php
public yy_r2_7(): mixed
```












***

### yy_r2_8



```php
public yy_r2_8(): mixed
```












***

### yy_r2_9



```php
public yy_r2_9(): mixed
```












***

### yylex3



```php
public yylex3(): mixed
```












***

### yy_r3_1



```php
public yy_r3_1(): mixed
```












***

### yylex4



```php
public yylex4(): mixed
```












***

### yy_r4_1



```php
public yy_r4_1(): mixed
```












***

### yy_r4_2



```php
public yy_r4_2(): mixed
```












***

### yy_r4_3



```php
public yy_r4_3(): mixed
```












***

### yylex5



```php
public yylex5(): mixed
```












***

### yy_r5_1



```php
public yy_r5_1(): mixed
```












***

### yy_r5_2



```php
public yy_r5_2(): mixed
```












***

### yylex6



```php
public yylex6(): mixed
```












***

### yy_r6_1



```php
public yy_r6_1(): mixed
```












***

### yy_r6_2



```php
public yy_r6_2(): mixed
```












***


***
> Automatically generated on 2025-03-15
