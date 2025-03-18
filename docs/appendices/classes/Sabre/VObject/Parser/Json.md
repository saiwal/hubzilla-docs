
# Json

Json Parser.

This parser parses both the jCal and jCard formats.

* Full name: `\Sabre\VObject\Parser\Json`
* Parent class: [`\Sabre\VObject\Parser\Parser`](./Parser.md)



## Properties


### input

The input data.

```php
protected array $input
```






***

### root

Root component.

```php
protected \Sabre\VObject\Document $root
```






***

## Methods


### parse

This method starts the parsing process.

```php
public parse(resource|string|array|null $input = null, int $options): \Sabre\VObject\Document
```

If the input was not supplied during construction, it's possible to pass
it here instead.

If either input or options are not supplied, the defaults will be used.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource&#124;string&#124;array&#124;null** |  |
| `$options` | **int** |  |





***

### parseComponent

Parses a component.

```php
public parseComponent(array $jComp): \Sabre\VObject\Component
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$jComp` | **array** |  |





***

### parseProperty

Parses properties.

```php
public parseProperty(array $jProp): \Sabre\VObject\Property
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$jProp` | **array** |  |





***

### setInput

Sets the input data.

```php
public setInput(resource|string|array $input): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource&#124;string&#124;array** |  |





***


## Inherited methods


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
> Automatically generated on 2025-03-18
