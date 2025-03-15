***

# NoAbstract

This exception is thrown when a user tries to set a privilege that's marked
as abstract.



* Full name: `\Sabre\DAVACL\Exception\NoAbstract`
* Parent class: [`\Sabre\DAV\Exception\PreconditionFailed`](../../DAV/Exception/PreconditionFailed.md)




## Methods


### serialize

Adds in extra information in the xml response.

```php
public serialize(\Sabre\DAV\Server $server, \DOMElement $errorNode): mixed
```

This method adds the {DAV:}no-abstract element as defined in rfc3744






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


***
> Automatically generated on 2025-03-15
