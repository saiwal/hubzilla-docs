
# Parser

Parses XML into something sane

This class can be overloaded with {@see \SimplePie\SimplePie::set_parser_class()}

* Full name: `\SimplePie\Parser`
* This class implements:
[`\SimplePie\RegistryAware`](./RegistryAware.md)



## Properties


### error_code



```php
public $error_code
```






***

### error_string



```php
public $error_string
```






***

### current_line



```php
public $current_line
```






***

### current_column



```php
public $current_column
```






***

### current_byte



```php
public $current_byte
```






***

### separator



```php
public $separator
```






***

### namespace



```php
public $namespace
```






***

### element



```php
public $element
```






***

### xml_base



```php
public $xml_base
```






***

### xml_base_explicit



```php
public $xml_base_explicit
```






***

### xml_lang



```php
public $xml_lang
```






***

### data



```php
public $data
```






***

### datas



```php
public $datas
```






***

### current_xhtml_construct



```php
public $current_xhtml_construct
```






***

### encoding



```php
public $encoding
```






***

### registry



```php
protected $registry
```






***

## Methods


### set_registry

Set the Registry into the class

```php
public set_registry(\SimplePie\Registry $registry): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$registry` | **\SimplePie\Registry** |  |





***

### parse



```php
public parse(mixed& $data, mixed $encoding, mixed $url = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$encoding` | **mixed** |  |
| `$url` | **mixed** |  |





***

### get_error_code



```php
public get_error_code(): mixed
```












***

### get_error_string



```php
public get_error_string(): mixed
```












***

### get_current_line



```php
public get_current_line(): mixed
```












***

### get_current_column



```php
public get_current_column(): mixed
```












***

### get_current_byte



```php
public get_current_byte(): mixed
```












***

### get_data



```php
public get_data(): mixed
```












***

### tag_open



```php
public tag_open(mixed $parser, mixed $tag, mixed $attributes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parser` | **mixed** |  |
| `$tag` | **mixed** |  |
| `$attributes` | **mixed** |  |





***

### cdata



```php
public cdata(mixed $parser, mixed $cdata): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parser` | **mixed** |  |
| `$cdata` | **mixed** |  |





***

### tag_close



```php
public tag_close(mixed $parser, mixed $tag): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parser` | **mixed** |  |
| `$tag` | **mixed** |  |





***

### split_ns



```php
public split_ns(mixed $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### parse_hcard



```php
private parse_hcard(mixed $data, mixed $category = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$category` | **mixed** |  |





***

### parse_microformats



```php
private parse_microformats(mixed& $data, mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$url` | **mixed** |  |





***

### declare_html_entities



```php
private declare_html_entities(): mixed
```












***


***
> Automatically generated on 2025-03-15
