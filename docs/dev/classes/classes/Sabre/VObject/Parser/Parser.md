
# Parser

Abstract parser.

This class serves as a base-class for the different parsers.

* Full name: `\Sabre\VObject\Parser\Parser`
* This class is an **Abstract class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`OPTION_FORGIVING`|public| |1|
|`OPTION_IGNORE_INVALID_LINES`|public| |2|

## Properties


### options

Bitmask of parser options.

```php
protected int $options
```






***

## Methods


### __construct

Creates the parser.

```php
public __construct(mixed $input = null, int $options): mixed
```

Optionally, it's possible to parse the input stream here.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$options` | **int** | any parser options (OPTION constants) |





***

### parse

This method starts the parsing process.

```php
public parse(mixed $input = null, int $options): array
```

If the input was not supplied during construction, it's possible to pass
it here instead.

If either input or options are not supplied, the defaults will be used.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$options` | **int** |  |





***

### setInput

Sets the input data.

```php
public setInput(mixed $input): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
