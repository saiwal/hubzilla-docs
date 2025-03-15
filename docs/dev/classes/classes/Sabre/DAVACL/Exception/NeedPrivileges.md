
# NeedPrivileges

NeedPrivileges.

The 403-need privileges is thrown when a user didn't have the appropriate
permissions to perform an operation

* Full name: `\Sabre\DAVACL\Exception\NeedPrivileges`
* Parent class: [`\Sabre\DAV\Exception\Forbidden`](../../DAV/Exception/Forbidden.md)



## Properties


### uri

The relevant uri.

```php
protected string $uri
```






***

### privileges

The privileges the user didn't have.

```php
protected array $privileges
```






***

## Methods


### __construct

Constructor.

```php
public __construct(string $uri, array $privileges): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$privileges` | **array** |  |





***

### serialize

Adds in extra information in the xml response.

```php
public serialize(\Sabre\DAV\Server $server, \DOMElement $errorNode): mixed
```

This method adds the {DAV:}need-privileges element as defined in rfc3744






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
