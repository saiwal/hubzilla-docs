***

# Base58





* Full name: `\StephenHill\Base58`

**See Also:**

* https://github.com/stephen-hill/base58php - 



## Properties


### service



```php
protected $service
```






***

## Methods


### __construct

Constructor

```php
public __construct(string $alphabet = null, \StephenHill\ServiceInterface $service = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$alphabet` | **string** | optional |
| `$service` | **\StephenHill\ServiceInterface** | optional |





***

### encode

Encode a string into base58.

```php
public encode(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | The string you wish to encode. |


**Return Value:**

The Base58 encoded string.




***

### decode

Decode base58 into a PHP string.

```php
public decode(string $base58): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base58` | **string** | The base58 encoded string. |


**Return Value:**

Returns the decoded string.




***


***
> Automatically generated on 2025-03-15
