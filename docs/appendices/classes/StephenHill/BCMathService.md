
# BCMathService





* Full name: `\StephenHill\BCMathService`
* This class implements:
[`\StephenHill\ServiceInterface`](./ServiceInterface.md)



## Properties


### alphabet



```php
protected string $alphabet
```






***

### base



```php
protected int $base
```






***

## Methods


### __construct

Constructor

```php
public __construct(string $alphabet = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$alphabet` | **string** | optional |





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
> Automatically generated on 2025-03-18
