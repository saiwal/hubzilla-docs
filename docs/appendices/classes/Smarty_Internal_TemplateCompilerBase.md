
# Smarty_Internal_TemplateCompilerBase

Main abstract compiler class



* Full name: `\Smarty_Internal_TemplateCompilerBase`
* This class is an **Abstract class**



## Properties


### _tag_objects

compile tag objects cache

```php
public static array $_tag_objects
```



* This property is **static**.


***

### prefixVariableNumber

counter for prefix variable number

```php
public static int $prefixVariableNumber
```



* This property is **static**.


***

### smarty

Smarty object

```php
public \Smarty $smarty
```






***

### parser

Parser object

```php
public \Smarty_Internal_Templateparser $parser
```






***

### nocache_hash

hash for nocache sections

```php
public mixed $nocache_hash
```






***

### suppressNocacheProcessing

suppress generation of nocache code

```php
public bool $suppressNocacheProcessing
```






***

### caching

caching enabled (copied from template object)

```php
public int $caching
```






***

### _tag_stack

tag stack

```php
public array $_tag_stack
```






***

### _tag_stack_count

tag stack count

```php
public array $_tag_stack_count
```






***

### required_plugins

Plugins used by template

```php
public array $required_plugins
```






***

### required_plugins_stack

Required plugins stack

```php
public array $required_plugins_stack
```






***

### template

current template

```php
public \Smarty_Internal_Template $template
```






***

### mergedSubTemplatesData

merged included sub template data

```php
public array $mergedSubTemplatesData
```






***

### mergedSubTemplatesCode

merged sub template code

```php
public array $mergedSubTemplatesCode
```






***

### templateProperties

collected template properties during compilation

```php
public array $templateProperties
```






***

### trace_line_offset

source line offset for error messages

```php
public int $trace_line_offset
```






***

### trace_uid

trace uid

```php
public string $trace_uid
```






***

### trace_filepath

trace file path

```php
public string $trace_filepath
```






***

### trace_stack

stack for tracing file and line of nested {block} tags

```php
public array $trace_stack
```






***

### default_handler_plugins

plugins loaded by default plugin handler

```php
public array $default_handler_plugins
```






***

### default_modifier_list

saved preprocessed modifier list

```php
public mixed $default_modifier_list
```






***

### forceNocache

force compilation of complete template as nocache

```php
public bool $forceNocache
```






***

### write_compiled_code

flag if compiled template file shall we written

```php
public bool $write_compiled_code
```






***

### tpl_function

Template functions

```php
public array $tpl_function
```






***

### called_functions

called sub functions from template function

```php
public array $called_functions
```






***

### blockOrFunctionCode

compiled template or block function code

```php
public string $blockOrFunctionCode
```






***

### modifier_plugins

flags for used modifier plugins

```php
public array $modifier_plugins
```






***

### known_modifier_type

type of already compiled modifier

```php
public array $known_modifier_type
```






***

### parent_compiler

parent compiler object for merged subtemplates and template functions

```php
public \Smarty_Internal_TemplateCompilerBase $parent_compiler
```






***

### nocache

Flag true when compiling nocache section

```php
public bool $nocache
```






***

### tag_nocache

Flag true when tag is compiled as nocache

```php
public bool $tag_nocache
```






***

### prefix_code

Compiled tag prefix code

```php
public array $prefix_code
```






***

### usedPrefixVariables

used prefix variables by current compiled tag

```php
public array $usedPrefixVariables
```






***

### prefixCodeStack

Prefix code  stack

```php
public array $prefixCodeStack
```






***

### has_code

Tag has compiled code

```php
public bool $has_code
```






***

### has_variable_string

A variable string was compiled

```php
public bool $has_variable_string
```






***

### variable_filter_stack

Stack for {setfilter} {/setfilter}

```php
public array $variable_filter_stack
```






***

### variable_filters

variable filters for {setfilter} {/setfilter}

```php
public array $variable_filters
```






***

### loopNesting

Nesting count of looping tags like {foreach}, {for}, {section}, {while}

```php
public int $loopNesting
```






***

### stripRegEx

Strip preg pattern

```php
public string $stripRegEx
```






***

### plugin_search_order

plugin search order

```php
public array $plugin_search_order
```






***

### _cache

General storage area for tag compiler plugins

```php
public array $_cache
```






***

### ldelPreg

Lexer preg pattern for left delimiter

```php
private string $ldelPreg
```






***

### rdelPreg

Lexer preg pattern for right delimiter

```php
private string $rdelPreg
```






***

### rdelLength

Length of right delimiter

```php
private int $rdelLength
```






***

### ldelLength

Length of left delimiter

```php
private int $ldelLength
```






***

### literalPreg

Lexer preg pattern for user literals

```php
private string $literalPreg
```






***

## Methods


### __construct

Initialize compiler

```php
public __construct(\Smarty $smarty): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | global instance |





***

### compileTemplate

Method to compile a Smarty template

```php
public compileTemplate(\Smarty_Internal_Template $template, bool $nocache = null, null|\Smarty_Internal_TemplateCompilerBase $parent_compiler = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** | template object to compile |
| `$nocache` | **bool** | true is shall be compiled in nocache mode |
| `$parent_compiler` | **null&#124;\Smarty_Internal_TemplateCompilerBase** |  |


**Return Value:**

true if compiling succeeded, false if it failed



**Throws:**

- [`Exception`](./Exception.md)



***

### compileTemplateSource

Compile template source and run optional post filter

```php
public compileTemplateSource(\Smarty_Internal_Template $template, null|bool $nocache = null, \Smarty_Internal_TemplateCompilerBase $parent_compiler = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |
| `$nocache` | **null&#124;bool** | flag if template must be compiled in nocache mode |
| `$parent_compiler` | **\Smarty_Internal_TemplateCompilerBase** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### postFilter

Optionally process compiled code by post filter

```php
public postFilter(string $code): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | compiled code |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### preFilter

Run optional prefilter

```php
public preFilter(string $_content): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_content` | **string** | template source |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### compileTag

Compile Tag
This is a call back from the lexer/parser

```php
public compileTag(string $tag, array $args, array $parameter = array()): string
```

Save current prefix code
Compile tag
Merge tag prefix code with saved one
(required nested tags in attributes)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | tag name |
| `$args` | **array** | array with tag attributes |
| `$parameter` | **array** | array with compilation parameter |


**Return Value:**

compiled code



**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)

- [`SmartyException`](./SmartyException.md)



***

### compileVariable

compile variable

```php
public compileVariable(string $variable): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$variable` | **string** |  |





***

### compileConfigVariable

compile config variable

```php
public compileConfigVariable(string $variable): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$variable` | **string** |  |





***

### compilePHPFunctionCall

compile PHP function call

```php
public compilePHPFunctionCall(string $name, array $parameter): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$parameter` | **array** |  |




**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***

### syntaxMatchesVariable

Determines whether the passed string represents a valid (PHP) variable.

```php
private syntaxMatchesVariable(mixed $string): bool
```

This is important, because `isset()` only works on variables and `empty()` can only be passed
a variable prior to php5.5






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### processText

This method is called from parser to process a text content section if strip is enabled
- remove text from inheritance child templates as they may generate output

```php
public processText(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### callTagCompiler

lazy loads internal compile plugin for tag and calls the compile method
compile objects cached for reuse.

```php
public callTagCompiler(string $tag, array $args, mixed $param1 = null, mixed $param2 = null, mixed $param3 = null): bool|string
```

class name format:  Smarty_Internal_Compile_TagName
plugin filename format: Smarty_Internal_TagName.php






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | tag name |
| `$args` | **array** | list of tag attributes |
| `$param1` | **mixed** | optional parameter |
| `$param2` | **mixed** | optional parameter |
| `$param3` | **mixed** | optional parameter |


**Return Value:**

compiled code or false



**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***

### getTagCompiler

lazy loads internal compile plugin for tag compile objects cached for reuse.

```php
public getTagCompiler(string $tag): bool|\Smarty_Internal_CompileBase
```

class name format:  Smarty_Internal_Compile_TagName
plugin filename format: Smarty_Internal_TagName.php






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | tag name |


**Return Value:**

tag compiler object or false if not found




***

### getPlugin

Check for plugins and return function name

```php
public getPlugin(mixed $plugin_name, string $plugin_type): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plugin_name` | **mixed** |  |
| `$plugin_type` | **string** | type of plugin |


**Return Value:**

call name of function



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### getPluginFromDefaultHandler

Check for plugins by default plugin handler

```php
public getPluginFromDefaultHandler(string $tag, string $plugin_type): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | name of tag |
| `$plugin_type` | **string** | type of plugin |


**Return Value:**

true if found



**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***

### appendCode

Append code segments and remove unneeded ?> <?php transitions

```php
public appendCode(string $left, string $right): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **string** |  |
| `$right` | **string** |  |





***

### processNocacheCode

Inject inline code for nocache template sections
This method gets the content of each template element from the parser.

```php
public processNocacheCode(string $content, bool $is_code): string
```

If the content is compiled code and it should be not cached the code is injected
into the rendered output.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **string** | content of template element |
| `$is_code` | **bool** | true if content is compiled code |


**Return Value:**

content




***

### getId

Get Id

```php
public getId(string $input): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** |  |





***

### getVariableName

Get variable name from string

```php
public getVariableName(string $input): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** |  |





***

### setNocacheInVariable

Set nocache flag in variable or create new variable

```php
public setNocacheInVariable(string $varName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$varName` | **string** |  |





***

### convertScope



```php
public convertScope(array $_attr, array $validScopes): int|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_attr` | **array** | tag attributes |
| `$validScopes` | **array** |  |




**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***

### makeNocacheCode

Generate nocache code string

```php
public makeNocacheCode(string $code): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | PHP code |





***

### trigger_template_error

display compiler error messages without dying
If parameter $args is empty it is a parser detected syntax error.

```php
public trigger_template_error(string $args = null, string $line = null, null|bool $tagline = null): mixed
```

In this case the parser is called to obtain information about expected tokens.
If parameter $args contains a string this is used as error message






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **string** | individual error message or null |
| `$line` | **string** | line-number |
| `$tagline` | **null&#124;bool** | if true the line number of last tag |




**Throws:**
<p>when an unexpected token is found</p>

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***

### getVarExport

Return var_export() value with all white spaces removed

```php
public getVarExport(mixed $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |





***

### enterDoubleQuote

enter double quoted string
 - save tag stack count

```php
public enterDoubleQuote(): mixed
```












***

### getTagStackCount

Return tag stack count

```php
public getTagStackCount(): int
```












***

### replaceDelimiter



```php
public replaceDelimiter(mixed $lexerPreg): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lexerPreg` | **mixed** |  |





***

### initDelimiterPreg

Build lexer regular expressions for left and right delimiter and user defined literals

```php
public initDelimiterPreg(): mixed
```












***

### leaveDoubleQuote

leave double quoted string
 - throw exception if block in string was not closed

```php
public leaveDoubleQuote(): mixed
```











**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)



***

### getLdelPreg

Get left delimiter preg

```php
public getLdelPreg(): string
```












***

### getRdelPreg

Get right delimiter preg

```php
public getRdelPreg(): string
```












***

### getLdelLength

Get length of left delimiter

```php
public getLdelLength(): int
```












***

### getRdelLength

Get length of right delimiter

```php
public getRdelLength(): int
```












***

### getOpenBlockTag

Get name of current open block tag

```php
public getOpenBlockTag(): string|bool
```












***

### isVariable

Check if $value contains variable elements

```php
public isVariable(mixed $value): bool|int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |





***

### getNewPrefixVariable

Get new prefix variable name

```php
public getNewPrefixVariable(): string
```












***

### getPrefixVariable

Get current prefix variable name

```php
public getPrefixVariable(): string
```












***

### appendPrefixCode

append  code to prefix buffer

```php
public appendPrefixCode(string $code): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |





***

### getPrefixCode

get prefix code string

```php
public getPrefixCode(): string
```












***

### saveRequiredPlugins

Save current required plugins

```php
public saveRequiredPlugins(bool $init = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$init` | **bool** | if true init required plugins |





***

### restoreRequiredPlugins

Restore required plugins

```php
public restoreRequiredPlugins(): mixed
```












***

### compileRequiredPlugins

Compile code to call Smarty_Internal_Template::_checkPlugins()
for required plugins

```php
public compileRequiredPlugins(): string
```












***

### compileCheckPlugins

Compile code to call Smarty_Internal_Template::_checkPlugins
  - checks if plugin is callable require otherwise

```php
public compileCheckPlugins(mixed $requiredPlugins): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$requiredPlugins` | **mixed** |  |





***

### doCompile

method to compile a Smarty template

```php
protected doCompile(mixed $_content, bool $isTemplateSource = false): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_content` | **mixed** | template source |
| `$isTemplateSource` | **bool** |  |


**Return Value:**

true if compiling succeeded, false if it failed




***

### cStyleComment



```php
public cStyleComment(mixed $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### compileTag2

Compile Tag

```php
private compileTag2(string $tag, array $args, array $parameter): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | tag name |
| `$args` | **array** | array with tag attributes |
| `$parameter` | **array** | array with compilation parameter |


**Return Value:**

compiled code



**Throws:**

- [`SmartyCompilerException`](./SmartyCompilerException.md)

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-18
