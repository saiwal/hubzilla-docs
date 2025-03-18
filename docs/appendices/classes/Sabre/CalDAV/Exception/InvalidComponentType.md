
# InvalidComponentType

InvalidComponentType.



* Full name: `\Sabre\CalDAV\Exception\InvalidComponentType`
* Parent class: [`\Sabre\DAV\Exception\Forbidden`](../../DAV/Exception/Forbidden.md)




## Methods


### serialize

Adds in extra information in the xml response.

```php
public serialize(\Sabre\DAV\Server $server, \DOMElement $errorNode): mixed
```

This method adds the {CALDAV:}supported-calendar-component as defined in rfc4791






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
> Automatically generated on 2025-03-18
