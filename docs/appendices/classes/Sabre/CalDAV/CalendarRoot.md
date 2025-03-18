
# CalendarRoot

Calendars collection.

This object is responsible for generating a list of calendar-homes for each
user.

This is the top-most node for the calendars tree. In most servers this class
represents the "/calendars" path.

* Full name: `\Sabre\CalDAV\CalendarRoot`
* Parent class: [`\Sabre\DAVACL\AbstractPrincipalCollection`](../DAVACL/AbstractPrincipalCollection.md)



## Properties


### caldavBackend

CalDAV backend.

```php
protected \Sabre\CalDAV\Backend\BackendInterface $caldavBackend
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\DAVACL\PrincipalBackend\BackendInterface $principalBackend, \Sabre\CalDAV\Backend\BackendInterface $caldavBackend, string $principalPrefix = &#039;principals&#039;): mixed
```

This constructor needs both an authentication and a caldav backend.

By default this class will show a list of calendar collections for
principals in the 'principals' collection. If your main principals are
actually located in a different path, use the $principalPrefix argument
to override this.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalBackend` | **\Sabre\DAVACL\PrincipalBackend\BackendInterface** |  |
| `$caldavBackend` | **\Sabre\CalDAV\Backend\BackendInterface** |  |
| `$principalPrefix` | **string** |  |





***

### getName

Returns the nodename.

```php
public getName(): string
```

We're overriding this, because the default will be the 'principalPrefix',
and we want it to be Sabre\CalDAV\Plugin::CALENDAR_ROOT










***

### getChildForPrincipal

This method returns a node for a principal.

```php
public getChildForPrincipal(array $principal): \Sabre\DAV\INode
```

The passed array contains principal information, and is guaranteed to
at least contain a uri item. Other properties may or may not be
supplied by the authentication backend.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principal` | **array** |  |





***


## Inherited methods


### getLastModified

Returns the last modification time as a unix timestamp.

```php
public getLastModified(): int
```

If the information is not available, return null.










***

### delete

Deletes the current node.

```php
public delete(): mixed
```











**Throws:**

- [`Forbidden`](../DAV/Exception/Forbidden.md)



***

### setName

Renames the node.

```php
public setName(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | The new name |




**Throws:**

- [`Forbidden`](../DAV/Exception/Forbidden.md)



***

### getChild

Returns a child object, by its name.

```php
public getChild(string $name): \Sabre\DAV\INode
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`NotFound`](../DAV/Exception/NotFound.md)



***

### childExists

Checks is a child-node exists.

```php
public childExists(string $name): bool
```

It is generally a good idea to try and override this. Usually it can be optimized.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### createFile

Creates a new file in the directory.

```php
public createFile(string $name, resource|string $data = null): string|null
```

Data will either be supplied as a stream resource, or in certain cases
as a string. Keep in mind that you may have to support either.

After successful creation of the file, you may choose to return the ETag
of the new file here.

The returned ETag must be surrounded by double-quotes (The quotes should
be part of the actual string).

If you cannot accurately determine the ETag, you should not return it.
If you don't store the file exactly as-is (you're transforming it
somehow) you should also not return an ETag.

This means that if a subsequent GET to this new file does not exactly
return the same contents of what was submitted here, you are strongly
recommended to omit the ETag.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Name of the file |
| `$data` | **resource&#124;string** | Initial payload |





***

### createDirectory

Creates a new subdirectory.

```php
public createDirectory(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`Forbidden`](../DAV/Exception/Forbidden.md)



***

### __construct

Creates the object.

```php
public __construct(\Sabre\DAVACL\PrincipalBackend\BackendInterface $principalBackend, string $principalPrefix = &#039;principals&#039;): mixed
```

This object must be passed the principal backend. This object will
filter all principals from a specified prefix ($principalPrefix). The
default is 'principals', if your principals are stored in a different
collection, override $principalPrefix






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalBackend` | **\Sabre\DAVACL\PrincipalBackend\BackendInterface** |  |
| `$principalPrefix` | **string** |  |





***

### getChildForPrincipal

This method returns a node for a principal.

```php
public getChildForPrincipal(array $principalInfo): \Sabre\DAV\INode
```

The passed array contains principal information, and is guaranteed to
at least contain a uri item. Other properties may or may not be
supplied by the authentication backend.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalInfo` | **array** |  |





***

### getName

Returns the name of this collection.

```php
public getName(): string
```












***

### getChildren

Return the list of users.

```php
public getChildren(): array
```












***

### searchPrincipals

This method is used to search for principals matching a set of
properties.

```php
public searchPrincipals(array $searchProperties, string $test = &#039;allof&#039;): array
```

This search is specifically used by RFC3744's principal-property-search
REPORT. You should at least allow searching on
http://sabredav.org/ns}email-address.

The actual search should be a unicode-non-case-sensitive search. The
keys in searchProperties are the WebDAV property names, while the values
are the property values to search on.

By default, if multiple properties are submitted to this method, the
various properties should be combined with 'AND'. If $test is set to
'anyof', it should be combined using 'OR'.

This method should simply return a list of 'child names', which may be
used to call $this->getChild in the future.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$searchProperties` | **array** |  |
| `$test` | **string** |  |





***

### findByUri

Finds a principal by its URI.

```php
public findByUri(string $uri): string
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





***


***
> Automatically generated on 2025-03-18
