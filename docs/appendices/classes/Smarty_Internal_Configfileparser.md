
# Smarty_Internal_Configfileparser

Smarty Internal Plugin Configfileparse

This is the config file parser.
It is generated from the smarty_internal_configfileparser.y file

* Full name: `\Smarty_Internal_Configfileparser`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TPC_OPENB`|public| |1|
|`TPC_SECTION`|public| |2|
|`TPC_CLOSEB`|public| |3|
|`TPC_DOT`|public| |4|
|`TPC_ID`|public| |5|
|`TPC_EQUAL`|public| |6|
|`TPC_FLOAT`|public| |7|
|`TPC_INT`|public| |8|
|`TPC_BOOL`|public| |9|
|`TPC_SINGLE_QUOTED_STRING`|public| |10|
|`TPC_DOUBLE_QUOTED_STRING`|public| |11|
|`TPC_TRIPPLE_QUOTES`|public| |12|
|`TPC_TRIPPLE_TEXT`|public| |13|
|`TPC_TRIPPLE_QUOTES_END`|public| |14|
|`TPC_NAKED_STRING`|public| |15|
|`TPC_OTHER`|public| |16|
|`TPC_NEWLINE`|public| |17|
|`TPC_COMMENTSTART`|public| |18|
|`YY_NO_ACTION`|public| |60|
|`YY_ACCEPT_ACTION`|public| |59|
|`YY_ERROR_ACTION`|public| |58|
|`YY_SZ_ACTTAB`|public| |38|
|`YY_SHIFT_USE_DFLT`|public| |-8|
|`YY_SHIFT_MAX`|public| |19|
|`YY_REDUCE_USE_DFLT`|public| |-17|
|`YY_REDUCE_MAX`|public| |10|
|`YYNOCODE`|public| |29|
|`YYSTACKDEPTH`|public| |100|
|`YYNSTATE`|public| |36|
|`YYNRULE`|public| |22|
|`YYERRORSYMBOL`|public| |19|
|`YYERRSYMDT`|public| |&#039;yy0&#039;|
|`YYFALLBACK`|public| |0|

## Properties


### yy_action



```php
public static $yy_action
```



* This property is **static**.


***

### yy_lookahead



```php
public static $yy_lookahead
```



* This property is **static**.


***

### yy_shift_ofst



```php
public static $yy_shift_ofst
```



* This property is **static**.


***

### yy_reduce_ofst



```php
public static $yy_reduce_ofst
```



* This property is **static**.


***

### yyExpectedTokens



```php
public static $yyExpectedTokens
```



* This property is **static**.


***

### yy_default



```php
public static $yy_default
```



* This property is **static**.


***

### yyFallback



```php
public static $yyFallback
```



* This property is **static**.


***

### yyRuleName



```php
public static $yyRuleName
```



* This property is **static**.


***

### yyRuleInfo



```php
public static $yyRuleInfo
```



* This property is **static**.


***

### yyReduceMap



```php
public static $yyReduceMap
```



* This property is **static**.


***

### escapes_single

helper map

```php
private static array $escapes_single
```



* This property is **static**.


***

### successful

result status

```php
public bool $successful
```






***

### retvalue

return value

```php
public mixed $retvalue
```






***

### yymajor



```php
public $yymajor
```






***

### compiler

compiler object

```php
public \Smarty_Internal_Config_File_Compiler $compiler
```






***

### smarty

smarty object

```php
public \Smarty $smarty
```






***

### yyTraceFILE



```php
public $yyTraceFILE
```






***

### yyTracePrompt



```php
public $yyTracePrompt
```






***

### yyidx



```php
public $yyidx
```






***

### yyerrcnt



```php
public $yyerrcnt
```






***

### yystack



```php
public $yystack
```






***

### yyTokenName



```php
public $yyTokenName
```






***

### lex

lexer object

```php
private \Smarty_Internal_Configfilelexer $lex
```






***

### internalError

internal error flag

```php
private bool $internalError
```






***

### configOverwrite

copy of config_overwrite property

```php
private bool $configOverwrite
```






***

### configReadHidden

copy of config_read_hidden property

```php
private bool $configReadHidden
```






***

### _retvalue



```php
private $_retvalue
```






***

## Methods


### __construct

constructor

```php
public __construct(\Smarty_Internal_Configfilelexer $lex, \Smarty_Internal_Config_File_Compiler $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lex` | **\Smarty_Internal_Configfilelexer** |  |
| `$compiler` | **\Smarty_Internal_Config_File_Compiler** |  |





***

### yy_destructor



```php
public static yy_destructor(mixed $yymajor, mixed $yypminor): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$yymajor` | **mixed** |  |
| `$yypminor` | **mixed** |  |





***

### parse_single_quoted_string

parse single quoted string
 remove outer quotes
 unescape inner quotes

```php
private static parse_single_quoted_string(string $qstr): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$qstr` | **string** |  |





***

### parse_double_quoted_string

parse double quoted string

```php
private static parse_double_quoted_string(string $qstr): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$qstr` | **string** |  |





***

### parse_tripple_double_quoted_string

parse triple quoted string

```php
private static parse_tripple_double_quoted_string(string $qstr): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$qstr` | **string** |  |





***

### Trace



```php
public Trace(mixed $TraceFILE, mixed $zTracePrompt): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$TraceFILE` | **mixed** |  |
| `$zTracePrompt` | **mixed** |  |





***

### PrintTrace



```php
public PrintTrace(): mixed
```












***

### tokenName



```php
public tokenName(mixed $tokenType): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokenType` | **mixed** |  |





***

### yy_pop_parser_stack



```php
public yy_pop_parser_stack(): mixed
```












***

### __destruct



```php
public __destruct(): mixed
```












***

### yy_get_expected_tokens



```php
public yy_get_expected_tokens(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### yy_is_expected_token



```php
public yy_is_expected_token(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### yy_find_shift_action



```php
public yy_find_shift_action(mixed $iLookAhead): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iLookAhead` | **mixed** |  |





***

### yy_find_reduce_action



```php
public yy_find_reduce_action(mixed $stateno, mixed $iLookAhead): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stateno` | **mixed** |  |
| `$iLookAhead` | **mixed** |  |





***

### yy_shift



```php
public yy_shift(mixed $yyNewState, mixed $yyMajor, mixed $yypMinor): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$yyNewState` | **mixed** |  |
| `$yyMajor` | **mixed** |  |
| `$yypMinor` | **mixed** |  |





***

### yy_r0



```php
public yy_r0(): mixed
```












***

### yy_r1



```php
public yy_r1(): mixed
```












***

### yy_r4



```php
public yy_r4(): mixed
```












***

### yy_r5



```php
public yy_r5(): mixed
```












***

### yy_r6



```php
public yy_r6(): mixed
```












***

### yy_r7



```php
public yy_r7(): mixed
```












***

### yy_r8



```php
public yy_r8(): mixed
```












***

### yy_r9



```php
public yy_r9(): mixed
```












***

### yy_r10



```php
public yy_r10(): mixed
```












***

### yy_r11



```php
public yy_r11(): mixed
```












***

### yy_r12



```php
public yy_r12(): mixed
```












***

### yy_r13



```php
public yy_r13(): mixed
```












***

### yy_r14



```php
public yy_r14(): mixed
```












***

### yy_r15



```php
public yy_r15(): mixed
```












***

### yy_r16



```php
public yy_r16(): mixed
```












***

### yy_r17



```php
public yy_r17(): mixed
```












***

### yy_reduce



```php
public yy_reduce(mixed $yyruleno): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$yyruleno` | **mixed** |  |





***

### yy_parse_failed



```php
public yy_parse_failed(): mixed
```












***

### yy_syntax_error



```php
public yy_syntax_error(mixed $yymajor, mixed $TOKEN): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$yymajor` | **mixed** |  |
| `$TOKEN` | **mixed** |  |





***

### yy_accept



```php
public yy_accept(): mixed
```












***

### doParse



```php
public doParse(mixed $yymajor, mixed $yytokenvalue): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$yymajor` | **mixed** |  |
| `$yytokenvalue` | **mixed** |  |





***

### parse_bool

parse optional boolean keywords

```php
private parse_bool(string $str): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***

### set_var

set a config variable in target array

```php
private set_var(array $var, array& $target_array): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **array** |  |
| `$target_array` | **array** |  |





***

### add_global_vars

add config variable to global vars

```php
private add_global_vars(array $vars): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vars` | **array** |  |





***

### add_section_vars

add config variable to section

```php
private add_section_vars(string $section_name, array $vars): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$section_name` | **string** |  |
| `$vars` | **array** |  |





***


***
> Automatically generated on 2025-03-18
