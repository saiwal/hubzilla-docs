***

# HTMLPurifier_Printer_ConfigForm





* Full name: `\HTMLPurifier_Printer_ConfigForm`
* Parent class: [`\HTMLPurifier_Printer`](./HTMLPurifier_Printer.md)



## Properties


### fields

Printers for specific fields.

```php
protected $fields
```






***

### docURL

Documentation URL, can have fragment tagged on end.

```php
protected $docURL
```






***

### name

Name of form element to stuff config in.

```php
protected $name
```






***

### compress

Whether or not to compress directive names, clipping them off
after a certain amount of letters. False to disable or integer letters
before clipping.

```php
protected $compress
```






***

### genConfig



```php
protected \HTMLPurifier_Config $genConfig
```






***

## Methods


### __construct

Initialize $generator.

```php
public __construct(string $name, string $doc_url = null, bool $compress = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Form element name for directives to be stuffed into |
| `$doc_url` | **string** | String documentation URL, will have fragment tagged on |
| `$compress` | **bool** | Integer max length before compressing a directive name, set to false to turn off |





***

### setTextareaDimensions

Sets default column and row size for textareas in sub-printers

```php
public setTextareaDimensions(mixed $cols = null, mixed $rows = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cols` | **mixed** | Integer columns of textarea, null to use default |
| `$rows` | **mixed** | Integer rows of textarea, null to use default |





***

### getCSS

Retrieves styling, in case it is not accessible by webserver

```php
public static getCSS(): mixed
```



* This method is **static**.








***

### getJavaScript

Retrieves JavaScript, in case it is not accessible by webserver

```php
public static getJavaScript(): mixed
```



* This method is **static**.








***

### render

Returns HTML output for a configuration form

```php
public render(\HTMLPurifier_Config|array $config, array|bool $allowed = true, bool $render_controls = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config&#124;array** | Configuration object of current form state, or an array<br />where [0] has an HTML namespace and [1] is being rendered. |
| `$allowed` | **array&#124;bool** | Optional namespace(s) and directives to restrict form to. |
| `$render_controls` | **bool** |  |





***

### renderNamespace

Renders a single namespace

```php
protected renderNamespace(mixed $ns, array $directives): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ns` | **mixed** | String namespace name |
| `$directives` | **array** | array of directives to values |





***


## Inherited methods


### __construct

Initialize $generator.

```php
public __construct(): mixed
```












***

### prepareGenerator

Give generator necessary configuration if possible

```php
public prepareGenerator(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### start

Returns a start tag

```php
protected start(string $tag, array $attr = array()): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | Tag name |
| `$attr` | **array** | Attribute array |





***

### end

Returns an end tag

```php
protected end(string $tag): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | Tag name |





***

### element

Prints a complete element with content inside

```php
protected element(string $tag, string $contents, array $attr = array(), bool $escape = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | Tag name |
| `$contents` | **string** | Element contents |
| `$attr` | **array** | Tag attributes |
| `$escape` | **bool** | whether or not to escape contents |





***

### elementEmpty



```php
protected elementEmpty(string $tag, array $attr = array()): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** |  |
| `$attr` | **array** |  |





***

### text



```php
protected text(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### row

Prints a simple key/value row in a table.

```php
protected row(string $name, mixed $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Key |
| `$value` | **mixed** | Value |





***

### escape

Escapes a string for HTML output.

```php
protected escape(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to escape |





***

### listify

Takes a list of strings and turns them into a single list

```php
protected listify(string[] $array, bool $polite = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **string[]** | List of strings |
| `$polite` | **bool** | Bool whether or not to add an end before the last |





***

### getClass

Retrieves the class of an object without prefixes, as well as metadata

```php
protected getClass(object $obj, string $sec_prefix = &#039;&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **object** | Object to determine class of |
| `$sec_prefix` | **string** | Further prefix to remove |





***


***
> Automatically generated on 2025-03-15
