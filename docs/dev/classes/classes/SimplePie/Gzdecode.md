***

# Gzdecode

Decode 'gzip' encoded HTTP data



* Full name: `\SimplePie\Gzdecode`

**See Also:**

* http://www.gzip.org/format.txt - 



## Properties


### compressed_data

Compressed data

```php
public string $compressed_data
```





**See Also:**

* \SimplePie\gzdecode::$data - 

***

### compressed_size

Size of compressed data

```php
public int $compressed_size
```






***

### min_compressed_size

Minimum size of a valid gzip string

```php
public int $min_compressed_size
```






***

### position

Current position of pointer

```php
public int $position
```






***

### flags

Flags (FLG)

```php
public int $flags
```






***

### data

Uncompressed data

```php
public string $data
```





**See Also:**

* \SimplePie\gzdecode::$compressed_data - 

***

### MTIME

Modified time

```php
public int $MTIME
```






***

### XFL

Extra Flags

```php
public int $XFL
```






***

### OS

Operating System

```php
public int $OS
```






***

### SI1

Subfield ID 1

```php
public string $SI1
```





**See Also:**

* \SimplePie\gzdecode::$extra_field - * \SimplePie\gzdecode::$SI2 - 

***

### SI2

Subfield ID 2

```php
public string $SI2
```





**See Also:**

* \SimplePie\gzdecode::$extra_field - * \SimplePie\gzdecode::$SI1 - 

***

### extra_field

Extra field content

```php
public string $extra_field
```





**See Also:**

* \SimplePie\gzdecode::$SI1 - * \SimplePie\gzdecode::$SI2 - 

***

### filename

Original filename

```php
public string $filename
```






***

### comment

Human readable comment

```php
public string $comment
```






***

## Methods


### __set

Don't allow anything to be set

```php
public __set(string $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### __construct

Set the compressed string and related properties

```php
public __construct(string $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### parse

Decode the GZIP stream

```php
public parse(): bool
```









**Return Value:**

Successfulness




***


***
> Automatically generated on 2025-03-15
