
# ANSI

Pure-PHP ANSI Decoder



* Full name: `\phpseclib\File\ANSI`



## Properties


### max_x

Max Width

```php
public int $max_x
```






***

### max_y

Max Height

```php
public int $max_y
```






***

### max_history

Max History

```php
public int $max_history
```






***

### history

History

```php
public array $history
```






***

### history_attrs

History Attributes

```php
public array $history_attrs
```






***

### x

Current Column

```php
public int $x
```






***

### y

Current Row

```php
public int $y
```






***

### old_x

Old Column

```php
public int $old_x
```






***

### old_y

Old Row

```php
public int $old_y
```






***

### base_attr_cell

An empty attribute cell

```php
public object $base_attr_cell
```






***

### attr_cell

The current attribute cell

```php
public object $attr_cell
```






***

### attr_row

An empty attribute row

```php
public array $attr_row
```






***

### screen

The current screen text

```php
public array $screen
```






***

### attrs

The current screen attributes

```php
public array $attrs
```






***

### ansi

Current ANSI code

```php
public string $ansi
```






***

### tokenization

Tokenization

```php
public array $tokenization
```






***

## Methods


### __construct

Default Constructor.

```php
public __construct(): \phpseclib\File\ANSI
```












***

### setDimensions

Set terminal width and height

```php
public setDimensions(int $x, int $y): mixed
```

Resets the screen as well






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** |  |
| `$y` | **int** |  |





***

### setHistory

Set the number of lines that should be logged past the terminal height

```php
public setHistory(int $history): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$history` | **int** |  |





***

### loadString

Load a string

```php
public loadString(string $source): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |





***

### appendString

Appdend a string

```php
public appendString(string $source): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |





***

### _newLine

Add a new line

```php
public _newLine(): mixed
```

Also update the $this->screen and $this->history buffers










***

### _processCoordinate

Returns the current coordinate without preformating

```php
public _processCoordinate(mixed $last_attr, mixed $cur_attr, mixed $char): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$last_attr` | **mixed** |  |
| `$cur_attr` | **mixed** |  |
| `$char` | **mixed** |  |





***

### _getScreen

Returns the current screen without preformating

```php
public _getScreen(): string
```












***

### getScreen

Returns the current screen

```php
public getScreen(): string
```












***

### getHistory

Returns the current screen and the x previous lines

```php
public getHistory(): string
```












***


***
> Automatically generated on 2025-03-18
