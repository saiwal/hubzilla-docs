***

# HTMLPurifier_Language

Represents a language and defines localizable string formatting and
other functions, as well as the localized messages for HTML Purifier.



* Full name: `\HTMLPurifier_Language`



## Properties


### code

ISO 639 language code of language. Prefers shortest possible version.

```php
public $code
```






***

### fallback

Fallback language code.

```php
public $fallback
```






***

### messages

Array of localizable messages.

```php
public $messages
```






***

### errorNames

Array of localizable error codes.

```php
public $errorNames
```






***

### error

True if no message file was found for this language, so English
is being used instead. Check this if you'd like to notify the
user that they've used a non-supported language.

```php
public $error
```






***

### _loaded

Has the language object been loaded yet?

```php
public $_loaded
```






***

### config



```php
protected $config
```






***

### context



```php
protected $context
```






***

## Methods


### __construct



```php
public __construct(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### load

Loads language object with necessary info from factory cache

```php
public load(): mixed
```












***

### getMessage

Retrieves a localised message.

```php
public getMessage(string $key): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | string identifier of message |


**Return Value:**

localised message




***

### getErrorName

Retrieves a localised error name.

```php
public getErrorName(int $int): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$int` | **int** | error number, corresponding to PHP&#039;s error reporting |


**Return Value:**

localised message




***

### listify

Converts an array list into a string readable representation

```php
public listify(array $array): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** |  |





***

### formatMessage

Formats a localised message with passed parameters

```php
public formatMessage(string $key, array $args = array()): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | string identifier of message |
| `$args` | **array** | Parameters to substitute in |


**Return Value:**

localised message




***


***
> Automatically generated on 2025-03-15
