
# SimpleTemplate





* Full name: `\Zotlabs\Render\SimpleTemplate`
* This class implements:
[`\Zotlabs\Render\TemplateEngine`](./TemplateEngine.md)



## Properties


### name



```php
public static $name
```



* This property is **static**.


***

### r



```php
public $r
```






***

### search



```php
public $search
```






***

### replace



```php
public $replace
```






***

### stack



```php
public $stack
```






***

### nodes



```php
public $nodes
```






***

### done



```php
public $done
```






***

### d



```php
public $d
```






***

### lang



```php
public $lang
```






***

### debug



```php
public $debug
```






***

## Methods


### _preg_error



```php
private _preg_error(): mixed
```












***

### _push_stack



```php
private _push_stack(): mixed
```












***

### _pop_stack



```php
private _pop_stack(): mixed
```












***

### _get_var



```php
private _get_var(mixed $name, mixed $retNoKey = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$retNoKey` | **mixed** |  |





***

### _replcb_if

IF node
\code
{{ if <$var> }}...[{{ else }} ...] {{ endif }}
{{ if <$var>==<val|$var> }}...[{{ else }} ...]{{ endif }}
{{ if <$var>!=<val|$var> }}...[{{ else }} ...]{{ endif }}
\endcode

```php
private _replcb_if(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### _replcb_for

FOR node
\code
{{ for <$var> as $name }}...{{ endfor }}
{{ for <$var> as $key=>$name }}...{{ endfor }}
\endcode

```php
private _replcb_for(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### _replcb_inc

INC node
\code
{{ inc <templatefile> [with $var1=$var2] }}{{ endinc }}
\endcode

```php
private _replcb_inc(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### _replcb_debug

DEBUG node
\code
{{ debug $var [$var [$var [...]]] }}{{ enddebug }}
\endcode
replace node with <pre>var_dump($var, $var, ...);</pre>

```php
private _replcb_debug(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### _replcb_node



```php
private _replcb_node(mixed $m): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **mixed** |  |





***

### _replcb



```php
private _replcb(mixed $m): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **mixed** |  |





***

### _build_nodes



```php
private _build_nodes(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### var_replace



```php
private var_replace(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### replace



```php
private replace(mixed $s, mixed $r): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |
| `$r` | **mixed** |  |





***

### replace_macros



```php
public replace_macros(mixed $s, mixed $r): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |
| `$r` | **mixed** |  |





***

### get_markup_template



```php
public get_markup_template(mixed $file, mixed $root = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |
| `$root` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
