
# getid3_handler





* Full name: `\ID3Parser\getID3\getid3_handler`
* This class is an **Abstract class**



## Properties


### getid3



```php
protected \ID3Parser\getID3\getID3 $getid3
```






***

### data_string_flag



```php
protected $data_string_flag
```






***

### data_string



```php
protected $data_string
```






***

### data_string_position



```php
protected $data_string_position
```






***

### data_string_length



```php
protected $data_string_length
```






***

### dependency_to



```php
private $dependency_to
```






***

## Methods


### __construct



```php
public __construct(\ID3Parser\getID3\getID3 $getid3, mixed $call_module = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$getid3` | **\ID3Parser\getID3\getID3** |  |
| `$call_module` | **mixed** |  |





***

### Analyze



```php
public Analyze(): mixed
```




* This method is **abstract**.







***

### AnalyzeString



```php
public AnalyzeString(mixed $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### setStringMode



```php
public setStringMode(mixed $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### ftell



```php
protected ftell(): mixed
```












***

### fread



```php
protected fread(mixed $bytes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **mixed** |  |





***

### fseek



```php
protected fseek(mixed $bytes, mixed $whence = SEEK_SET): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **mixed** |  |
| `$whence` | **mixed** |  |





***

### feof



```php
protected feof(): mixed
```












***

### isDependencyFor



```php
final protected isDependencyFor(mixed $module): mixed
```





* This method is **final**.


**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$module` | **mixed** |  |





***

### error



```php
protected error(mixed $text): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **mixed** |  |





***

### warning



```php
protected warning(mixed $text): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **mixed** |  |





***

### notice



```php
protected notice(mixed $text): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
