
# StreamLogger

A logger that prints to a PHP stream (for instance stderr)



* Full name: `\ScssPhp\ScssPhp\Logger\StreamLogger`
* This class implements:
[`\ScssPhp\ScssPhp\Logger\LoggerInterface`](./LoggerInterface.md)



## Properties


### stream



```php
private $stream
```






***

### closeOnDestruct



```php
private $closeOnDestruct
```






***

## Methods


### __construct



```php
public __construct(resource $stream, bool $closeOnDestruct = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stream` | **resource** | A stream resource |
| `$closeOnDestruct` | **bool** | If true, takes ownership of the stream and close it on destruct to avoid leaks. |





***

### warn

Emits a warning with the given message.

```php
public warn(mixed $message, mixed $deprecation = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **mixed** |  |
| `$deprecation` | **mixed** |  |





***

### debug

Emits a debugging message.

```php
public debug(mixed $message): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
