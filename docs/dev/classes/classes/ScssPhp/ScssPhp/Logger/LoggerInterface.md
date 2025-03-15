***

# LoggerInterface

Interface implemented by loggers for warnings and debug messages.

The official Sass implementation recommends that loggers report the
messages immediately rather than waiting for the end of the
compilation, to provide a better debugging experience when the
compilation does not end (error or infinite loop after the warning
for instance).

* Full name: `\ScssPhp\ScssPhp\Logger\LoggerInterface`



## Methods


### warn

Emits a warning with the given message.

```php
public warn(string $message, bool $deprecation = false): void
```

If $deprecation is true, it indicates that this is a deprecation
warning. Implementations should surface all this information to
the end user.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |
| `$deprecation` | **bool** |  |





***

### debug

Emits a debugging message.

```php
public debug(string $message): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |





***


***
> Automatically generated on 2025-03-15
