***

# RequestInterface

The RequestInterface represents a HTTP request.



* Full name: `\Sabre\HTTP\RequestInterface`
* Parent interfaces: [`\Sabre\HTTP\MessageInterface`](./MessageInterface.md)


## Methods


### getMethod

Returns the current HTTP method.

```php
public getMethod(): string
```












***

### setMethod

Sets the HTTP method.

```php
public setMethod(string $method): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **string** |  |





***

### getUrl

Returns the request url.

```php
public getUrl(): string
```












***

### setUrl

Sets the request url.

```php
public setUrl(string $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |





***

### getAbsoluteUrl

Returns the absolute url.

```php
public getAbsoluteUrl(): string
```












***

### setAbsoluteUrl

Sets the absolute url.

```php
public setAbsoluteUrl(string $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |





***

### getBaseUrl

Returns the current base url.

```php
public getBaseUrl(): string
```












***

### setBaseUrl

Sets a base url.

```php
public setBaseUrl(string $url): mixed
```

This url is used for relative path calculations.

The base url should default to /






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |





***

### getPath

Returns the relative path.

```php
public getPath(): string
```

This is being calculated using the base url. This path will not start
with a slash, so it will always return something like
'example/path.html'.

If the full path is equal to the base url, this method will return an
empty string.

This method will also urldecode the path, and if the url was encoded as
ISO-8859-1, it will convert it to UTF-8.

If the path is outside of the base url, a LogicException will be thrown.










***

### getQueryParameters

Returns the list of query parameters.

```php
public getQueryParameters(): array
```

This is equivalent to PHP's $_GET superglobal.










***

### getPostData

Returns the POST data.

```php
public getPostData(): array
```

This is equivalent to PHP's $_POST superglobal.










***

### setPostData

Sets the post data.

```php
public setPostData(array $postData): mixed
```

This is equivalent to PHP's $_POST superglobal.

This would not have been needed, if POST data was accessible as
php://input, but unfortunately we need to special case it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$postData` | **array** |  |





***

### getRawServerValue

Returns an item from the _SERVER array.

```php
public getRawServerValue(string $valueName): string|null
```

If the value does not exist in the array, null is returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$valueName` | **string** |  |





***

### setRawServerData

Sets the _SERVER array.

```php
public setRawServerData(array $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array** |  |





***


## Inherited methods


### getBodyAsStream

Returns the body as a readable stream resource.

```php
public getBodyAsStream(): resource
```

Note that the stream may not be rewindable, and therefore may only be
read once.










***

### getBodyAsString

Returns the body as a string.

```php
public getBodyAsString(): string
```

Note that because the underlying data may be based on a stream, this
method could only work correctly the first time.










***

### getBody

Returns the message body, as its internal representation.

```php
public getBody(): resource|string|callable
```

This could be either a string, a stream or a callback writing the body to php://output










***

### setBody

Updates the body resource with a new stream.

```php
public setBody(resource|string|callable $body): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$body` | **resource&#124;string&#124;callable** |  |





***

### getHeaders

Returns all the HTTP headers as an array.

```php
public getHeaders(): array
```

Every header is returned as an array, with one or more values.










***

### hasHeader

Will return true or false, depending on if a HTTP header exists.

```php
public hasHeader(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getHeader

Returns a specific HTTP header, based on its name.

```php
public getHeader(string $name): string|null
```

The name must be treated as case-insensitive.
If the header does not exist, this method must return null.

If a header appeared more than once in a HTTP request, this method will
concatenate all the values with a comma.

Note that this not make sense for all headers. Some, such as
`Set-Cookie` cannot be logically combined with a comma. In those cases
you *should* use getHeaderAsArray().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getHeaderAsArray

Returns a HTTP header as an array.

```php
public getHeaderAsArray(string $name): string[]
```

For every time the HTTP header appeared in the request or response, an
item will appear in the array.

If the header did not exist, this method will return an empty array.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### setHeader

Updates a HTTP header.

```php
public setHeader(string $name, string|string[] $value): mixed
```

The case-sensitivity of the name value must be retained as-is.

If the header already existed, it will be overwritten.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **string&#124;string[]** |  |





***

### setHeaders

Sets a new set of HTTP headers.

```php
public setHeaders(array $headers): mixed
```

The headers array should contain headernames for keys, and their value
should be specified as either a string or an array.

Any header that already existed will be overwritten.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **array** |  |





***

### addHeader

Adds a HTTP header.

```php
public addHeader(string $name, string|string[] $value): mixed
```

This method will not overwrite any existing HTTP header, but instead add
another value. Individual values can be retrieved with
getHeadersAsArray.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **string&#124;string[]** |  |





***

### addHeaders

Adds a new set of HTTP headers.

```php
public addHeaders(array $headers): mixed
```

Any existing headers will not be overwritten.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **array** |  |





***

### removeHeader

Removes a HTTP header.

```php
public removeHeader(string $name): bool
```

The specified header name must be treated as case-insensitive.
This method should return true if the header was successfully deleted,
and false if the header did not exist.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### setHttpVersion

Sets the HTTP version.

```php
public setHttpVersion(string $version): mixed
```

Should be 1.0, 1.1 or 2.0.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **string** |  |





***

### getHttpVersion

Returns the HTTP version.

```php
public getHttpVersion(): string
```












***


***
> Automatically generated on 2025-03-15
