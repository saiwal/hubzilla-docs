***

# SimplePie_HTTP_Parser

HTTP Response Parser



* Full name: `\SimplePie_HTTP_Parser`
* Parent class: [`\SimplePie\HTTP\Parser`](./SimplePie/HTTP/Parser.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


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
