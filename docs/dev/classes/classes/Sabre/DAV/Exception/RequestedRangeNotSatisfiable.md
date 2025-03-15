
# RequestedRangeNotSatisfiable

RequestedRangeNotSatisfiable.

This exception is normally thrown when the user
request a range that is out of the entity bounds.

* Full name: `\Sabre\DAV\Exception\RequestedRangeNotSatisfiable`
* Parent class: [`\Sabre\DAV\Exception`](../Exception.md)




## Methods


### getHTTPCode

returns the http statuscode for this exception.

```php
public getHTTPCode(): int
```












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
