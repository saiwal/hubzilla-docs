***

# Parser

Parses the XML Declaration



* Full name: `\SimplePie\XML\Declaration\Parser`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`STATE_BEFORE_VERSION_NAME`|private| |&#039;before_version_name&#039;|
|`STATE_VERSION_NAME`|private| |&#039;version_name&#039;|
|`STATE_VERSION_EQUALS`|private| |&#039;version_equals&#039;|
|`STATE_VERSION_VALUE`|private| |&#039;version_value&#039;|
|`STATE_ENCODING_NAME`|private| |&#039;encoding_name&#039;|
|`STATE_EMIT`|private| |&#039;emit&#039;|
|`STATE_ENCODING_EQUALS`|private| |&#039;encoding_equals&#039;|
|`STATE_STANDALONE_NAME`|private| |&#039;standalone_name&#039;|
|`STATE_ENCODING_VALUE`|private| |&#039;encoding_value&#039;|
|`STATE_STANDALONE_EQUALS`|private| |&#039;standalone_equals&#039;|
|`STATE_STANDALONE_VALUE`|private| |&#039;standalone_value&#039;|
|`STATE_ERROR`|private| |false|

## Properties


### version

XML Version

```php
public string $version
```






***

### encoding

Encoding

```php
public string $encoding
```






***

### standalone

Standalone

```php
public bool $standalone
```






***

### state

Current state of the state machine

```php
public self::STATE_* $state
```






***

### data

Input data

```php
public string $data
```






***

### data_length

Input data length (to avoid calling strlen() everytime this is needed)

```php
public int $data_length
```






***

### position

Current position of the pointer

```php
public int $position
```






***

## Methods


### __construct

Create an instance of the class with the input data

```php
public __construct(string $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Input data |





***

### parse

Parse the input data

```php
public parse(): bool
```









**Return Value:**

true on success, false on failure




***

### has_data

Check whether there is data beyond the pointer

```php
public has_data(): bool
```









**Return Value:**

true if there is further data, false if not




***

### skip_whitespace

Advance past any whitespace

```php
public skip_whitespace(): int
```









**Return Value:**

Number of whitespace characters passed




***

### get_value

Read value

```php
public get_value(): mixed
```












***

### before_version_name



```php
public before_version_name(): mixed
```












***

### version_name



```php
public version_name(): mixed
```












***

### version_equals



```php
public version_equals(): mixed
```












***

### version_value



```php
public version_value(): mixed
```












***

### encoding_name



```php
public encoding_name(): mixed
```












***

### encoding_equals



```php
public encoding_equals(): mixed
```












***

### encoding_value



```php
public encoding_value(): mixed
```












***

### standalone_name



```php
public standalone_name(): mixed
```












***

### standalone_equals



```php
public standalone_equals(): mixed
```












***

### standalone_value



```php
public standalone_value(): mixed
```












***


***
> Automatically generated on 2025-03-15
