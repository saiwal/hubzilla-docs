
# Parser

HTTP Response Parser



* Full name: `\SimplePie\HTTP\Parser`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`STATE_HTTP_VERSION`|private| |&#039;http_version&#039;|
|`STATE_STATUS`|private| |&#039;status&#039;|
|`STATE_REASON`|private| |&#039;reason&#039;|
|`STATE_NEW_LINE`|private| |&#039;new_line&#039;|
|`STATE_BODY`|private| |&#039;body&#039;|
|`STATE_NAME`|private| |&#039;name&#039;|
|`STATE_VALUE`|private| |&#039;value&#039;|
|`STATE_VALUE_CHAR`|private| |&#039;value_char&#039;|
|`STATE_QUOTE`|private| |&#039;quote&#039;|
|`STATE_QUOTE_ESCAPED`|private| |&#039;quote_escaped&#039;|
|`STATE_QUOTE_CHAR`|private| |&#039;quote_char&#039;|
|`STATE_CHUNKED`|private| |&#039;chunked&#039;|
|`STATE_EMIT`|private| |&#039;emit&#039;|
|`STATE_ERROR`|private| |false|

## Properties


### http_version

HTTP Version

```php
public float $http_version
```






***

### status_code

Status code

```php
public int $status_code
```






***

### reason

Reason phrase

```php
public string $reason
```






***

### headers

Key/value pairs of the headers

```php
public array $headers
```






***

### body

Body of the response

```php
public string $body
```






***

### state

Current state of the state machine

```php
protected self::STATE_* $state
```






***

### data

Input data

```php
protected string $data
```






***

### data_length

Input data length (to avoid calling strlen() everytime this is needed)

```php
protected int $data_length
```






***

### position

Current position of the pointer

```php
protected int $position
```






***

### name

Name of the hedaer currently being parsed

```php
protected string $name
```






***

### value

Value of the hedaer currently being parsed

```php
protected string $value
```






***

## Methods


### __construct

Create an instance of the class with the input data

```php
public __construct(string $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Input data |





***

### parse

Parse the input data

```php
public parse(): bool
```









**Return Value:**

true on success, false on failure




***

### has_data

Check whether there is data beyond the pointer

```php
protected has_data(): bool
```









**Return Value:**

true if there is further data, false if not




***

### is_linear_whitespace

See if the next character is LWS

```php
protected is_linear_whitespace(): bool
```









**Return Value:**

true if the next character is LWS, false if not




***

### http_version

Parse the HTTP version

```php
protected http_version(): mixed
```












***

### status

Parse the status code

```php
protected status(): mixed
```












***

### reason

Parse the reason phrase

```php
protected reason(): mixed
```












***

### new_line

Deal with a new line, shifting data around as needed

```php
protected new_line(): mixed
```












***

### name

Parse a header name

```php
protected name(): mixed
```












***

### linear_whitespace

Parse LWS, replacing consecutive LWS characters with a single space

```php
protected linear_whitespace(): mixed
```












***

### value

See what state to move to while within non-quoted header values

```php
protected value(): mixed
```












***

### value_char

Parse a header value while outside quotes

```php
protected value_char(): mixed
```












***

### quote

See what state to move to while within quoted header values

```php
protected quote(): mixed
```












***

### quote_char

Parse a header value while within quotes

```php
protected quote_char(): mixed
```












***

### quote_escaped

Parse an escaped character within quotes

```php
protected quote_escaped(): mixed
```












***

### body

Parse the body

```php
protected body(): mixed
```












***

### chunked

Parsed a "Transfer-Encoding: chunked" body

```php
protected chunked(): mixed
```












***

### prepareHeaders

Prepare headers (take care of proxies headers)

```php
public static prepareHeaders(string $headers, int $count = 1): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **string** | Raw headers |
| `$count` | **int** | Redirection count. Default to 1. |





***


***
> Automatically generated on 2025-03-15
