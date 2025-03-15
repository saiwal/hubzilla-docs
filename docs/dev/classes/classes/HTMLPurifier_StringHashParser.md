
# HTMLPurifier_StringHashParser

Parses string hash files. File format is as such:

DefaultKeyValue
     KEY: Value
     KEY2: Value2
     --MULTILINE-KEY--
     Multiline
     value.

Which would output something similar to:

     array(
         'ID' => 'DefaultKeyValue',
         'KEY' => 'Value',
         'KEY2' => 'Value2',
         'MULTILINE-KEY' => "Multiline\nvalue.\n",
     )

We use this as an easy to use file-format for configuration schema
files, but the class itself is usage agnostic.

You can use ---- to forcibly terminate parsing of a single string-hash;
this marker is used in multi string-hashes to delimit boundaries.

* Full name: `\HTMLPurifier_StringHashParser`



## Properties


### default



```php
public $default
```






***

## Methods


### parseFile

Parses a file that contains a single string-hash.

```php
public parseFile(string $file): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***

### parseMultiFile

Parses a file that contains multiple string-hashes delimited by '----'

```php
public parseMultiFile(string $file): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***

### parseHandle

Internal parser that acepts a file handle.

```php
protected parseHandle(resource $fh): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fh` | **resource** | File handle with pointer at start of valid string-hash<br />block. |





***


***
> Automatically generated on 2025-03-15
