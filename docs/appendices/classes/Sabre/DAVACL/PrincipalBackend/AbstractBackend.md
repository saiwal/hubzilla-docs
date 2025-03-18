
# AbstractBackend

Abstract Principal Backend.

Currently this class has no function. It's here for consistency and so we
have a non-bc-breaking way to add a default generic implementation to
functions we may add in the future.

* Full name: `\Sabre\DAVACL\PrincipalBackend\AbstractBackend`
* This class implements:
[`\Sabre\DAVACL\PrincipalBackend\BackendInterface`](./BackendInterface.md)
* This class is an **Abstract class**




## Methods


### findByUri

Finds a principal by its URI.

```php
public findByUri(string $uri, string $principalPrefix): string|null
```

This method may receive any type of uri, but mailto: addresses will be
the most common.

Implementation of this API is optional. It is currently used by the
CalDAV system to find principals based on their email addresses. If this
API is not implemented, some features may not work correctly.

This method must return a relative principal path, or null, if the
principal was not found or you refuse to find it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$principalPrefix` | **string** |  |





***


***
> Automatically generated on 2025-03-18
