
# getID3





* Full name: `\ID3Parser\getID3\getID3`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`FREAD_BUFFER_SIZE`|public| |32768|

## Properties


### encoding



```php
private $encoding
```






***

### option_fread_buffer_size



```php
private $option_fread_buffer_size
```






***

### filename



```php
public $filename
```






***

### fp



```php
public $fp
```






***

### info



```php
public $info
```






***

### memory_limit



```php
public $memory_limit
```






***

### startup_error



```php
protected $startup_error
```






***

### startup_warning



```php
protected $startup_warning
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### fread_buffer_size



```php
public fread_buffer_size(): mixed
```












***

### setOption



```php
public setOption(mixed $optArray): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$optArray` | **mixed** |  |





***

### openfile



```php
public openfile(mixed $filename): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **mixed** |  |





***

### analyze



```php
public analyze(mixed $filename): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **mixed** |  |





***

### error



```php
public error(mixed $message): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **mixed** |  |





***

### warning



```php
public warning(mixed $message): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **mixed** |  |





***

### CleanUp



```php
private CleanUp(): mixed
```












***


***
> Automatically generated on 2025-03-15
