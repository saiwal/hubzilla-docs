***

# InsufficientStorage

InsufficientStorage.

This Exception can be thrown, when for example a harddisk is full or a quota is exceeded

* Full name: `\Sabre\DAV\Exception\InsufficientStorage`
* Parent class: [`\Sabre\DAV\Exception`](../Exception.md)




## Methods


### getHTTPCode

Returns the HTTP statuscode for this exception.

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
