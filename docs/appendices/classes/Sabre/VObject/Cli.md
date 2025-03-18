
# Cli

This is the CLI interface for sabre-vobject.



* Full name: `\Sabre\VObject\Cli`



## Properties


### quiet

No output.

```php
protected bool $quiet
```






***

### showHelp

Help display.

```php
protected bool $showHelp
```






***

### format

Whether to spit out 'mimedir' or 'json' format.

```php
protected string $format
```






***

### pretty

JSON pretty print.

```php
protected bool $pretty
```






***

### inputPath

Source file.

```php
protected string $inputPath
```






***

### outputPath

Destination file.

```php
protected string $outputPath
```






***

### stdout

output stream.

```php
protected resource $stdout
```






***

### stdin

stdin.

```php
protected resource $stdin
```






***

### stderr

stderr.

```php
protected resource $stderr
```






***

### inputFormat

Input format (one of json or mimedir).

```php
protected string $inputFormat
```






***

### forgiving

Makes the parser less strict.

```php
protected bool $forgiving
```






***

### parser



```php
protected $parser
```






***

## Methods


### main

Main function.

```php
public main(array $argv): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$argv` | **array** |  |





***

### showHelp

Shows the help message.

```php
protected showHelp(): mixed
```












***

### validate

Validates a VObject file.

```php
protected validate(\Sabre\VObject\Component $vObj): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vObj` | **\Sabre\VObject\Component** |  |





***

### repair

Repairs a VObject file.

```php
protected repair(\Sabre\VObject\Component $vObj): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vObj` | **\Sabre\VObject\Component** |  |





***

### convert

Converts a vObject file to a new format.

```php
protected convert(\Sabre\VObject\Component $vObj): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vObj` | **\Sabre\VObject\Component** |  |





***

### color

Colorizes a file.

```php
protected color(\Sabre\VObject\Component $vObj): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vObj` | **\Sabre\VObject\Component** |  |





***

### colorize

Returns an ansi color string for a color name.

```php
protected colorize(string $color, mixed $str, mixed $resetTo = &#039;default&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **string** |  |
| `$str` | **mixed** |  |
| `$resetTo` | **mixed** |  |





***

### cWrite

Writes out a string in specific color.

```php
protected cWrite(string $color, string $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **string** |  |
| `$str` | **string** |  |





***

### serializeComponent



```php
protected serializeComponent(\Sabre\VObject\Component $vObj): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vObj` | **\Sabre\VObject\Component** |  |





***

### serializeProperty

Colorizes a property.

```php
protected serializeProperty(\Sabre\VObject\Property $property): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **\Sabre\VObject\Property** |  |





***

### parseArguments

Parses the list of arguments.

```php
protected parseArguments(array $argv): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$argv` | **array** |  |





***

### readInput

Reads the input file.

```php
protected readInput(): \Sabre\VObject\Component
```












***

### log

Sends a message to STDERR.

```php
protected log(string $msg, mixed $color = &#039;default&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **string** |  |
| `$color` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
