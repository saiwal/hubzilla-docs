
# Smarty_Internal_Templatelexer

Smarty_Internal_Templatelexer
This is the template file lexer.

It is generated from the smarty_internal_templatelexer.plex file

* Full name: `\Smarty_Internal_Templatelexer`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TEXT`|public| |1|
|`TAG`|public| |2|
|`TAGBODY`|public| |3|
|`LITERAL`|public| |4|
|`DOUBLEQUOTEDSTRING`|public| |5|

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

### taglineno

tag start line

```php
public $taglineno
```






***

### phpType

php code type

```php
public string $phpType
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

### compiler

compiler object

```php
public \Smarty_Internal_TemplateCompilerBase $compiler
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

### is_xml

XML flag true while processing xml

```php
public bool $is_xml
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

### literal_cnt

literal tag nesting level

```php
private int $literal_cnt
```






***

### yy_global_pattern1

preg token pattern for state TEXT

```php
private string $yy_global_pattern1
```






***

### yy_global_pattern2

preg token pattern for state TAG

```php
private string $yy_global_pattern2
```






***

### yy_global_pattern3

preg token pattern for state TAGBODY

```php
private string $yy_global_pattern3
```






***

### yy_global_pattern4

preg token pattern for state LITERAL

```php
private string $yy_global_pattern4
```






***

### yy_global_pattern5

preg token pattern for state DOUBLEQUOTEDSTRING

```php
private null $yy_global_pattern5
```






***

### yy_global_text

preg token pattern for text

```php
private null $yy_global_text
```






***

### yy_global_literal

preg token pattern for literal

```php
private null $yy_global_literal
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
public __construct(string $source, \Smarty_Internal_TemplateCompilerBase $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** | template source |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |





***

### PrintTrace

open lexer/parser trace file

```php
public PrintTrace(): mixed
```












***

### replace

replace placeholders with runtime preg  code

```php
public replace(string $preg): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$preg` | **string** |  |





***

### isAutoLiteral

check if current value is an autoliteral left delimiter

```php
public isAutoLiteral(): bool
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

### yy_r1_4



```php
public yy_r1_4(): mixed
```












***

### yy_r1_6



```php
public yy_r1_6(): mixed
```












***

### yy_r1_8



```php
public yy_r1_8(): mixed
```












***

### yy_r1_10



```php
public yy_r1_10(): mixed
```












***

### yy_r1_12



```php
public yy_r1_12(): mixed
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

### yy_r2_4



```php
public yy_r2_4(): mixed
```












***

### yy_r2_6



```php
public yy_r2_6(): mixed
```












***

### yy_r2_8



```php
public yy_r2_8(): mixed
```












***

### yy_r2_10



```php
public yy_r2_10(): mixed
```












***

### yy_r2_12



```php
public yy_r2_12(): mixed
```












***

### yy_r2_15



```php
public yy_r2_15(): mixed
```












***

### yy_r2_18



```php
public yy_r2_18(): mixed
```












***

### yy_r2_20



```php
public yy_r2_20(): mixed
```












***

### yy_r2_23



```php
public yy_r2_23(): mixed
```












***

### yy_r2_25



```php
public yy_r2_25(): mixed
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

### yy_r3_2



```php
public yy_r3_2(): mixed
```












***

### yy_r3_4



```php
public yy_r3_4(): mixed
```












***

### yy_r3_5



```php
public yy_r3_5(): mixed
```












***

### yy_r3_6



```php
public yy_r3_6(): mixed
```












***

### yy_r3_7



```php
public yy_r3_7(): mixed
```












***

### yy_r3_8



```php
public yy_r3_8(): mixed
```












***

### yy_r3_9



```php
public yy_r3_9(): mixed
```












***

### yy_r3_10



```php
public yy_r3_10(): mixed
```












***

### yy_r3_11



```php
public yy_r3_11(): mixed
```












***

### yy_r3_12



```php
public yy_r3_12(): mixed
```












***

### yy_r3_13



```php
public yy_r3_13(): mixed
```












***

### yy_r3_15



```php
public yy_r3_15(): mixed
```












***

### yy_r3_17



```php
public yy_r3_17(): mixed
```












***

### yy_r3_20



```php
public yy_r3_20(): mixed
```












***

### yy_r3_23



```php
public yy_r3_23(): mixed
```












***

### yy_r3_24



```php
public yy_r3_24(): mixed
```












***

### yy_r3_28



```php
public yy_r3_28(): mixed
```












***

### yy_r3_29



```php
public yy_r3_29(): mixed
```












***

### yy_r3_30



```php
public yy_r3_30(): mixed
```












***

### yy_r3_31



```php
public yy_r3_31(): mixed
```












***

### yy_r3_32



```php
public yy_r3_32(): mixed
```












***

### yy_r3_33



```php
public yy_r3_33(): mixed
```












***

### yy_r3_34



```php
public yy_r3_34(): mixed
```












***

### yy_r3_35



```php
public yy_r3_35(): mixed
```












***

### yy_r3_37



```php
public yy_r3_37(): mixed
```












***

### yy_r3_39



```php
public yy_r3_39(): mixed
```












***

### yy_r3_41



```php
public yy_r3_41(): mixed
```












***

### yy_r3_42



```php
public yy_r3_42(): mixed
```












***

### yy_r3_43



```php
public yy_r3_43(): mixed
```












***

### yy_r3_44



```php
public yy_r3_44(): mixed
```












***

### yy_r3_45



```php
public yy_r3_45(): mixed
```












***

### yy_r3_48



```php
public yy_r3_48(): mixed
```












***

### yy_r3_49



```php
public yy_r3_49(): mixed
```












***

### yy_r3_50



```php
public yy_r3_50(): mixed
```












***

### yy_r3_51



```php
public yy_r3_51(): mixed
```












***

### yy_r3_52



```php
public yy_r3_52(): mixed
```












***

### yy_r3_53



```php
public yy_r3_53(): mixed
```












***

### yy_r3_54



```php
public yy_r3_54(): mixed
```












***

### yy_r3_55



```php
public yy_r3_55(): mixed
```












***

### yy_r3_56



```php
public yy_r3_56(): mixed
```












***

### yy_r3_57



```php
public yy_r3_57(): mixed
```












***

### yy_r3_58



```php
public yy_r3_58(): mixed
```












***

### yy_r3_59



```php
public yy_r3_59(): mixed
```












***

### yy_r3_60



```php
public yy_r3_60(): mixed
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

### yy_r4_3



```php
public yy_r4_3(): mixed
```












***

### yy_r4_5



```php
public yy_r4_5(): mixed
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

### yy_r5_3



```php
public yy_r5_3(): mixed
```












***

### yy_r5_5



```php
public yy_r5_5(): mixed
```












***

### yy_r5_7



```php
public yy_r5_7(): mixed
```












***

### yy_r5_9



```php
public yy_r5_9(): mixed
```












***

### yy_r5_11



```php
public yy_r5_11(): mixed
```












***

### yy_r5_13



```php
public yy_r5_13(): mixed
```












***

### yy_r5_14



```php
public yy_r5_14(): mixed
```












***

### yy_r5_15



```php
public yy_r5_15(): mixed
```












***

### yy_r5_16



```php
public yy_r5_16(): mixed
```












***

### yy_r5_17



```php
public yy_r5_17(): mixed
```












***

### yy_r5_22



```php
public yy_r5_22(): mixed
```












***


***
> Automatically generated on 2025-03-18
