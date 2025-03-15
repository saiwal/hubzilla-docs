
# SimplePie_Parser

Parses XML into something sane



* Full name: `\SimplePie_Parser`
* Parent class: [`\SimplePie\Parser`](./SimplePie/Parser.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


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
