
# PreconditionFailed

PreconditionFailed.

This exception is normally thrown when a client submitted a conditional request,
like for example an If, If-None-Match or If-Match header, which caused the HTTP
request to not execute (the condition of the header failed)

* Full name: `\Sabre\DAV\Exception\PreconditionFailed`
* Parent class: [`\Sabre\DAV\Exception`](../Exception.md)



## Properties


### header

When this exception is thrown, the header-name might be set.

```php
public string $header
```

This allows the exception-catching code to determine which HTTP header
caused the exception.




***

## Methods


### __construct

Create the exception.

```php
public __construct(string $message, string $header = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |
| `$header` | **string** |  |





***

### getHTTPCode

Returns the HTTP statuscode for this exception.

```php
public getHTTPCode(): int
```












***

### serialize

This method allows the exception to include additional information into the WebDAV error response.

```php
public serialize(\Sabre\DAV\Server $server, \DOMElement $errorNode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |
| `$errorNode` | **\DOMElement** |  |





***


## Inherited methods


### getHTTPCode

Returns the HTTP statuscode for this exception.

```php
public getHTTPCode(): int
```












***

### serialize

This method allows the exception to include additional information into the WebDAV error response.

```php
public serialize(\Sabre\DAV\Server $server, \DOMElement $errorNode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |
| `$errorNode` | **\DOMElement** |  |





***

### getHTTPHeaders

This method allows the exception to return any extra HTTP response headers.

```php
public getHTTPHeaders(\Sabre\DAV\Server $server): array
```

The headers must be returned as an array.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***


***
> Automatically generated on 2025-03-15
