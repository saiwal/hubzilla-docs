***

# BackendInterface

Implement this interface to create your own principal backends.

Creating backends for principals is entirely optional. You can also
implement Sabre\DAVACL\IPrincipal directly. This interface is used solely by
Sabre\DAVACL\AbstractPrincipalCollection.

* Full name: `\Sabre\DAVACL\PrincipalBackend\BackendInterface`



## Methods


### getPrincipalsByPrefix

Returns a list of principals based on a prefix.

```php
public getPrincipalsByPrefix(string $prefixPath): array
```

This prefix will often contain something like 'principals'. You are only
expected to return principals that are in this base path.

You are expected to return at least a 'uri' for every user, you can
return any additional properties if you wish so. Common properties are:
  {DAV:}displayname
  {http://sabredav.org/ns}email-address - This is a custom SabreDAV
    field that's actually injected in a number of other properties. If
    you have an email address, use this property.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefixPath` | **string** |  |





***

### getPrincipalByPath

Returns a specific principal, specified by it's path.

```php
public getPrincipalByPath(string $path): array
```

The returned structure should be the exact same as from
getPrincipalsByPrefix.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### updatePrincipal

Updates one or more webdav properties on a principal.

```php
public updatePrincipal(string $path, \Sabre\DAV\PropPatch $propPatch): mixed
```

The list of mutations is stored in a Sabre\DAV\PropPatch object.
To do the actual updates, you must tell this object which properties
you're going to process with the handle() method.

Calling the handle method is like telling the PropPatch object "I
promise I can handle updating this property".

Read the PropPatch documentation for more info and examples.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### searchPrincipals

This method is used to search for principals matching a set of
properties.

```php
public searchPrincipals(string $prefixPath, array $searchProperties, string $test = &#039;allof&#039;): array
```

This search is specifically used by RFC3744's principal-property-search
REPORT.

The actual search should be a unicode-non-case-sensitive search. The
keys in searchProperties are the WebDAV property names, while the values
are the property values to search on.

By default, if multiple properties are submitted to this method, the
various properties should be combined with 'AND'. If $test is set to
'anyof', it should be combined using 'OR'.

This method should simply return an array with full principal uri's.

If somebody attempted to search on a property the backend does not
support, you should simply return 0 results.

You can also just return 0 results if you choose to not support
searching at all, but keep in mind that this may stop certain features
from working.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefixPath` | **string** |  |
| `$searchProperties` | **array** |  |
| `$test` | **string** |  |





***

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

### getGroupMemberSet

Returns the list of members for a group-principal.

```php
public getGroupMemberSet(string $principal): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principal` | **string** |  |





***

### getGroupMembership

Returns the list of groups a principal is a member of.

```php
public getGroupMembership(string $principal): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principal` | **string** |  |





***

### setGroupMemberSet

Updates the list of group members for a group principal.

```php
public setGroupMemberSet(string $principal, array $members): mixed
```

The principals should be passed as a list of uri's.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principal` | **string** |  |
| `$members` | **array** |  |





***


***
> Automatically generated on 2025-03-15
