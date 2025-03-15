***

# IPrincipalCollection

Principal Collection interface.

Implement this interface to ensure that your principal collection can be
searched using the principal-property-search REPORT.

* Full name: `\Sabre\DAVACL\IPrincipalCollection`
* Parent interfaces: [`\Sabre\DAV\ICollection`](../DAV/ICollection.md)


## Methods


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


## Inherited methods


### delete

Deleted the current node.

```php
public delete(): mixed
```












***

### getName

Returns the name of the node.

```php
public getName(): string
```

This is used to generate the url.










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





***

### getLastModified

Returns the last modification time, as a unix timestamp. Return null
if the information is not available.

```php
public getLastModified(): int|null
```












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





***

### getChild

Returns a specific child node, referenced by its name.

```php
public getChild(string $name): \Sabre\DAV\INode
```

This method must throw Sabre\DAV\Exception\NotFound if the node does not
exist.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getChildren

Returns an array with all the child nodes.

```php
public getChildren(): \Sabre\DAV\INode[]
```












***

### childExists

Checks if a child-node with the specified name exists.

```php
public childExists(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***


***
> Automatically generated on 2025-03-15
