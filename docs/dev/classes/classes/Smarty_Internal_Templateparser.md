
# Smarty_Internal_Templateparser

Smarty Template Parser Class

This is the template parser.
It is generated from the smarty_internal_templateparser.y file

* Full name: `\Smarty_Internal_Templateparser`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`ERR1`|public| |&#039;Security error: Call to private object member not allowed&#039;|
|`ERR2`|public| |&#039;Security error: Call to dynamic object member not allowed&#039;|
|`TP_VERT`|public| |1|
|`TP_COLON`|public| |2|
|`TP_TEXT`|public| |3|
|`TP_STRIPON`|public| |4|
|`TP_STRIPOFF`|public| |5|
|`TP_LITERALSTART`|public| |6|
|`TP_LITERALEND`|public| |7|
|`TP_LITERAL`|public| |8|
|`TP_SIMPELOUTPUT`|public| |9|
|`TP_SIMPLETAG`|public| |10|
|`TP_SMARTYBLOCKCHILDPARENT`|public| |11|
|`TP_LDEL`|public| |12|
|`TP_RDEL`|public| |13|
|`TP_DOLLARID`|public| |14|
|`TP_EQUAL`|public| |15|
|`TP_ID`|public| |16|
|`TP_PTR`|public| |17|
|`TP_LDELMAKENOCACHE`|public| |18|
|`TP_LDELIF`|public| |19|
|`TP_LDELFOR`|public| |20|
|`TP_SEMICOLON`|public| |21|
|`TP_INCDEC`|public| |22|
|`TP_TO`|public| |23|
|`TP_STEP`|public| |24|
|`TP_LDELFOREACH`|public| |25|
|`TP_SPACE`|public| |26|
|`TP_AS`|public| |27|
|`TP_APTR`|public| |28|
|`TP_LDELSETFILTER`|public| |29|
|`TP_CLOSETAG`|public| |30|
|`TP_LDELSLASH`|public| |31|
|`TP_ATTR`|public| |32|
|`TP_INTEGER`|public| |33|
|`TP_COMMA`|public| |34|
|`TP_OPENP`|public| |35|
|`TP_CLOSEP`|public| |36|
|`TP_MATH`|public| |37|
|`TP_UNIMATH`|public| |38|
|`TP_ISIN`|public| |39|
|`TP_QMARK`|public| |40|
|`TP_NOT`|public| |41|
|`TP_TYPECAST`|public| |42|
|`TP_HEX`|public| |43|
|`TP_DOT`|public| |44|
|`TP_INSTANCEOF`|public| |45|
|`TP_SINGLEQUOTESTRING`|public| |46|
|`TP_DOUBLECOLON`|public| |47|
|`TP_NAMESPACE`|public| |48|
|`TP_AT`|public| |49|
|`TP_HATCH`|public| |50|
|`TP_OPENB`|public| |51|
|`TP_CLOSEB`|public| |52|
|`TP_DOLLAR`|public| |53|
|`TP_LOGOP`|public| |54|
|`TP_SLOGOP`|public| |55|
|`TP_TLOGOP`|public| |56|
|`TP_SINGLECOND`|public| |57|
|`TP_ARRAYOPEN`|public| |58|
|`TP_QUOTE`|public| |59|
|`TP_BACKTICK`|public| |60|
|`YY_NO_ACTION`|public| |514|
|`YY_ACCEPT_ACTION`|public| |513|
|`YY_ERROR_ACTION`|public| |512|
|`YY_SZ_ACTTAB`|public| |1997|
|`YY_SHIFT_USE_DFLT`|public| |-22|
|`YY_SHIFT_MAX`|public| |230|
|`YY_REDUCE_USE_DFLT`|public| |-89|
|`YY_REDUCE_MAX`|public| |178|
|`YYNOCODE`|public| |109|
|`YYSTACKDEPTH`|public| |500|
|`YYNSTATE`|public| |326|
|`YYNRULE`|public| |186|
|`YYERRORSYMBOL`|public| |61|
|`YYERRSYMDT`|public| |&#039;yy0&#039;|
|`YYFALLBACK`|public| |0|

## Properties


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

### last_index

last index of array variable

```php
public mixed $last_index
```






***

### last_variable

last variable name

```php
public string $last_variable
```






***

### root_buffer

root parse tree buffer

```php
public \Smarty_Internal_ParseTree_Template $root_buffer
```






***

### current_buffer

current parse tree object

```php
public \Smarty_Internal_ParseTree $current_buffer
```






***

### lex

lexer object

```php
public \Smarty_Internal_Templatelexer $lex
```






***

### internalError

internal error flag

```php
private bool $internalError
```






***

### strip

{strip} status

```php
public bool $strip
```






***

### compiler

compiler object

```php
public \Smarty_Internal_TemplateCompilerBase $compiler
```






***

### smarty

smarty object

```php
public \Smarty $smarty
```






***

### template

template object

```php
public \Smarty_Internal_Template $template
```






***

### block_nesting_level

block nesting level

```php
public int $block_nesting_level
```






***

### security

security object

```php
public \Smarty_Security $security
```






***

### template_prefix

template prefix array

```php
public \Smarty_Internal_ParseTree[] $template_prefix
```






***

### template_postfix

template prefix array

```php
public \Smarty_Internal_ParseTree[] $template_postfix
```






***

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

### _retvalue



```php
private $_retvalue
```






***

## Methods


### __construct

constructor

```php
public __construct(\Smarty_Internal_Templatelexer $lex, \Smarty_Internal_TemplateCompilerBase $compiler): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lex` | **\Smarty_Internal_Templatelexer** |  |
| `$compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |





***

### insertPhpCode

insert PHP code in current buffer

```php
public insertPhpCode(string $code): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |





***

### errorRunDown

error rundown

```php
public errorRunDown(): mixed
```












***

### mergePrefixCode

merge PHP code with prefix code and return parse tree tag object

```php
public mergePrefixCode(string $code): \Smarty_Internal_ParseTree_Tag
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |





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

### yy_r2



```php
public yy_r2(): mixed
```












***

### yy_r3



```php
public yy_r3(): mixed
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

### yy_r18



```php
public yy_r18(): mixed
```












***

### yy_r19



```php
public yy_r19(): mixed
```












***

### yy_r20



```php
public yy_r20(): mixed
```












***

### yy_r24



```php
public yy_r24(): mixed
```












***

### yy_r25



```php
public yy_r25(): mixed
```












***

### yy_r26



```php
public yy_r26(): mixed
```












***

### yy_r27



```php
public yy_r27(): mixed
```












***

### yy_r28



```php
public yy_r28(): mixed
```












***

### yy_r29



```php
public yy_r29(): mixed
```












***

### yy_r30



```php
public yy_r30(): mixed
```












***

### yy_r31



```php
public yy_r31(): mixed
```












***

### yy_r32



```php
public yy_r32(): mixed
```












***

### yy_r34



```php
public yy_r34(): mixed
```












***

### yy_r35



```php
public yy_r35(): mixed
```












***

### yy_r37



```php
public yy_r37(): mixed
```












***

### yy_r38



```php
public yy_r38(): mixed
```












***

### yy_r39



```php
public yy_r39(): mixed
```












***

### yy_r40



```php
public yy_r40(): mixed
```












***

### yy_r41



```php
public yy_r41(): mixed
```












***

### yy_r42



```php
public yy_r42(): mixed
```












***

### yy_r43



```php
public yy_r43(): mixed
```












***

### yy_r44



```php
public yy_r44(): mixed
```












***

### yy_r45



```php
public yy_r45(): mixed
```












***

### yy_r46



```php
public yy_r46(): mixed
```












***

### yy_r47



```php
public yy_r47(): mixed
```












***

### yy_r48



```php
public yy_r48(): mixed
```












***

### yy_r49



```php
public yy_r49(): mixed
```












***

### yy_r50



```php
public yy_r50(): mixed
```












***

### yy_r51



```php
public yy_r51(): mixed
```












***

### yy_r52



```php
public yy_r52(): mixed
```












***

### yy_r53



```php
public yy_r53(): mixed
```












***

### yy_r55



```php
public yy_r55(): mixed
```












***

### yy_r58



```php
public yy_r58(): mixed
```












***

### yy_r60



```php
public yy_r60(): mixed
```












***

### yy_r61



```php
public yy_r61(): mixed
```












***

### yy_r63



```php
public yy_r63(): mixed
```












***

### yy_r64



```php
public yy_r64(): mixed
```












***

### yy_r67



```php
public yy_r67(): mixed
```












***

### yy_r68



```php
public yy_r68(): mixed
```












***

### yy_r70



```php
public yy_r70(): mixed
```












***

### yy_r71



```php
public yy_r71(): mixed
```












***

### yy_r72



```php
public yy_r72(): mixed
```












***

### yy_r73



```php
public yy_r73(): mixed
```












***

### yy_r74



```php
public yy_r74(): mixed
```












***

### yy_r75



```php
public yy_r75(): mixed
```












***

### yy_r76



```php
public yy_r76(): mixed
```












***

### yy_r78



```php
public yy_r78(): mixed
```












***

### yy_r79



```php
public yy_r79(): mixed
```












***

### yy_r84



```php
public yy_r84(): mixed
```












***

### yy_r85



```php
public yy_r85(): mixed
```












***

### yy_r86



```php
public yy_r86(): mixed
```












***

### yy_r87



```php
public yy_r87(): mixed
```












***

### yy_r89



```php
public yy_r89(): mixed
```












***

### yy_r90



```php
public yy_r90(): mixed
```












***

### yy_r94



```php
public yy_r94(): mixed
```












***

### yy_r95



```php
public yy_r95(): mixed
```












***

### yy_r96



```php
public yy_r96(): mixed
```












***

### yy_r99



```php
public yy_r99(): mixed
```












***

### yy_r101



```php
public yy_r101(): mixed
```












***

### yy_r102



```php
public yy_r102(): mixed
```












***

### yy_r103



```php
public yy_r103(): mixed
```












***

### yy_r104



```php
public yy_r104(): mixed
```












***

### yy_r106



```php
public yy_r106(): mixed
```












***

### yy_r107



```php
public yy_r107(): mixed
```












***

### yy_r108



```php
public yy_r108(): mixed
```












***

### yy_r109



```php
public yy_r109(): mixed
```












***

### yy_r110



```php
public yy_r110(): mixed
```












***

### yy_r111



```php
public yy_r111(): mixed
```












***

### yy_r113



```php
public yy_r113(): mixed
```












***

### yy_r114



```php
public yy_r114(): mixed
```












***

### yy_r115



```php
public yy_r115(): mixed
```












***

### yy_r116



```php
public yy_r116(): mixed
```












***

### yy_r117



```php
public yy_r117(): mixed
```












***

### yy_r118



```php
public yy_r118(): mixed
```












***

### yy_r119



```php
public yy_r119(): mixed
```












***

### yy_r120



```php
public yy_r120(): mixed
```












***

### yy_r121



```php
public yy_r121(): mixed
```












***

### yy_r122



```php
public yy_r122(): mixed
```












***

### yy_r124



```php
public yy_r124(): mixed
```












***

### yy_r128



```php
public yy_r128(): mixed
```












***

### yy_r129



```php
public yy_r129(): mixed
```












***

### yy_r130



```php
public yy_r130(): mixed
```












***

### yy_r131



```php
public yy_r131(): mixed
```












***

### yy_r133



```php
public yy_r133(): mixed
```












***

### yy_r134



```php
public yy_r134(): mixed
```












***

### yy_r135



```php
public yy_r135(): mixed
```












***

### yy_r136



```php
public yy_r136(): mixed
```












***

### yy_r137



```php
public yy_r137(): mixed
```












***

### yy_r138



```php
public yy_r138(): mixed
```












***

### yy_r139



```php
public yy_r139(): mixed
```












***

### yy_r140



```php
public yy_r140(): mixed
```












***

### yy_r141



```php
public yy_r141(): mixed
```












***

### yy_r142



```php
public yy_r142(): mixed
```












***

### yy_r143



```php
public yy_r143(): mixed
```












***

### yy_r144



```php
public yy_r144(): mixed
```












***

### yy_r145



```php
public yy_r145(): mixed
```












***

### yy_r146



```php
public yy_r146(): mixed
```












***

### yy_r149



```php
public yy_r149(): mixed
```












***

### yy_r150



```php
public yy_r150(): mixed
```












***

### yy_r152



```php
public yy_r152(): mixed
```












***

### yy_r153



```php
public yy_r153(): mixed
```












***

### yy_r156



```php
public yy_r156(): mixed
```












***

### yy_r158



```php
public yy_r158(): mixed
```












***

### yy_r159



```php
public yy_r159(): mixed
```












***

### yy_r160



```php
public yy_r160(): mixed
```












***

### yy_r161



```php
public yy_r161(): mixed
```












***

### yy_r162



```php
public yy_r162(): mixed
```












***

### yy_r163



```php
public yy_r163(): mixed
```












***

### yy_r164



```php
public yy_r164(): mixed
```












***

### yy_r165



```php
public yy_r165(): mixed
```












***

### yy_r166



```php
public yy_r166(): mixed
```












***

### yy_r167



```php
public yy_r167(): mixed
```












***

### yy_r170



```php
public yy_r170(): mixed
```












***

### yy_r172



```php
public yy_r172(): mixed
```












***

### yy_r173



```php
public yy_r173(): mixed
```












***

### yy_r176



```php
public yy_r176(): mixed
```












***

### yy_r177



```php
public yy_r177(): mixed
```












***

### yy_r178



```php
public yy_r178(): mixed
```












***

### yy_r179



```php
public yy_r179(): mixed
```












***

### yy_r180



```php
public yy_r180(): mixed
```












***

### yy_r181



```php
public yy_r181(): mixed
```












***

### yy_r184



```php
public yy_r184(): mixed
```












***

### yy_r185



```php
public yy_r185(): mixed
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


***
> Automatically generated on 2025-03-15
