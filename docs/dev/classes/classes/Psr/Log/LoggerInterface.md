
# LoggerInterface

Describes a logger instance.

The message MUST be a string or object implementing __toString().

The message MAY contain placeholders in the form: {foo} where foo
will be replaced by the context data in key "foo".

The context array can contain arbitrary data. The only assumption that
can be made by implementors is that if an Exception instance is given
to produce a stack trace, it MUST be in a key named "exception".

See https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-3-logger-interface.md
for the full interface specification.

* Full name: `\Psr\Log\LoggerInterface`



## Methods


### emergency

System is unusable.

```php
public emergency(string|\Stringable $message, array $context = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### alert

Action must be taken immediately.

```php
public alert(string|\Stringable $message, array $context = []): void
```

Example: Entire website down, database unavailable, etc. This should
trigger the SMS alerts and wake you up.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### critical

Critical conditions.

```php
public critical(string|\Stringable $message, array $context = []): void
```

Example: Application component unavailable, unexpected exception.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### error

Runtime errors that do not require immediate action but should typically
be logged and monitored.

```php
public error(string|\Stringable $message, array $context = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### warning

Exceptional occurrences that are not errors.

```php
public warning(string|\Stringable $message, array $context = []): void
```

Example: Use of deprecated APIs, poor use of an API, undesirable things
that are not necessarily wrong.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### notice

Normal but significant events.

```php
public notice(string|\Stringable $message, array $context = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### info

Interesting events.

```php
public info(string|\Stringable $message, array $context = []): void
```

Example: User logs in, SQL logs.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### debug

Detailed debug information.

```php
public debug(string|\Stringable $message, array $context = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |





***

### log

Logs with an arbitrary level.

```php
public log(mixed $level, string|\Stringable $message, array $context = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$level` | **mixed** |  |
| `$message` | **string&#124;\Stringable** |  |
| `$context` | **array** |  |




**Throws:**

- [`InvalidArgumentException`](./InvalidArgumentException.md)



***


***
> Automatically generated on 2025-03-15
