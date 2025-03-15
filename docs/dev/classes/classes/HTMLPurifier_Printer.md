
# HTMLPurifier_Printer





* Full name: `\HTMLPurifier_Printer`



## Properties


### generator

For HTML generation convenience funcs.

```php
protected $generator
```






***

### config

For easy access.

```php
protected $config
```






***

## Methods


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
