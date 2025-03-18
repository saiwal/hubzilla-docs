
# ConflictingLock

ConflictingLock.

Similar to  the Locked exception, this exception thrown when a LOCK request
was made, on a resource which was already locked

* Full name: `\Sabre\DAV\Exception\ConflictingLock`
* Parent class: [`\Sabre\DAV\Exception\Locked`](./Locked.md)




## Methods


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

### __construct

Creates the exception.

```php
public __construct(\Sabre\DAV\Locks\LockInfo $lock = null): mixed
```

A LockInfo object should be passed if the user should be informed
which lock actually has the file locked.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lock` | **\Sabre\DAV\Locks\LockInfo** |  |





***


***
> Automatically generated on 2025-03-18
