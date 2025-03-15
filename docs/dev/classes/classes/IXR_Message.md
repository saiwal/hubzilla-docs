***

# IXR_Message

IXR_MESSAGE



* Full name: `\IXR_Message`



## Properties


### message



```php
public $message
```






***

### messageType



```php
public $messageType
```






***

### faultCode



```php
public $faultCode
```






***

### faultString



```php
public $faultString
```






***

### methodName



```php
public $methodName
```






***

### params



```php
public $params
```






***

### _arraystructs



```php
public $_arraystructs
```






***

### _arraystructstypes



```php
public $_arraystructstypes
```






***

### _currentStructName



```php
public $_currentStructName
```






***

### _param



```php
public $_param
```






***

### _value



```php
public $_value
```






***

### _currentTag



```php
public $_currentTag
```






***

### _currentTagContents



```php
public $_currentTagContents
```






***

### _parser



```php
public $_parser
```






***

## Methods


### __construct



```php
public __construct(mixed $message): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **mixed** |  |





***

### parse



```php
public parse(): mixed
```












***

### tag_open



```php
public tag_open(mixed $parser, mixed $tag, mixed $attr): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parser` | **mixed** |  |
| `$tag` | **mixed** |  |
| `$attr` | **mixed** |  |





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


***
> Automatically generated on 2025-03-15
