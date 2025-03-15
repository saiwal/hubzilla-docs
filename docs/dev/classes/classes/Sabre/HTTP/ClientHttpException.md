
# ClientHttpException

This exception represents a HTTP error coming from the Client.

By default the Client will not emit these, this has to be explicitly enabled
with the setThrowExceptions method.

* Full name: `\Sabre\HTTP\ClientHttpException`
* Parent class: [`Exception`](../../Exception.md)
* This class implements:
[`\Sabre\HTTP\HttpException`](./HttpException.md)



## Properties


### response

Response object.

```php
protected \Sabre\HTTP\ResponseInterface $response
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### getHttpStatus

The http status code for the error.

```php
public getHttpStatus(): string|null
```












***

### getResponse

Returns the full response object.

```php
public getResponse(): \Sabre\HTTP\ResponseInterface
```












***


***
> Automatically generated on 2025-03-15
