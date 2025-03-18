
# QuietLogger

A logger that silently ignores all messages.



* Full name: `\ScssPhp\ScssPhp\Logger\QuietLogger`
* This class implements:
[`\ScssPhp\ScssPhp\Logger\LoggerInterface`](./LoggerInterface.md)




## Methods


### warn

Emits a warning with the given message.

```php
public warn(mixed $message, mixed $deprecation = false): void
```

If $deprecation is true, it indicates that this is a deprecation
warning. Implementations should surface all this information to
the end user.






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
