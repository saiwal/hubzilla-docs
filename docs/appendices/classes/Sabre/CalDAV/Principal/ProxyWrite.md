
# ProxyWrite

ProxyWrite principal.

This class represents a principal group, hosted under the main principal.
This is needed to implement 'Calendar delegation' support. This class is
instantiated by User.

* Full name: `\Sabre\CalDAV\Principal\ProxyWrite`
* This class implements:
[`\Sabre\CalDAV\Principal\IProxyWrite`](./IProxyWrite.md)



## Properties


### principalInfo

Parent principal information.

```php
protected array $principalInfo
```






***

### principalBackend

Principal Backend.

```php
protected \Sabre\DAVACL\PrincipalBackend\BackendInterface $principalBackend
```






***

## Methods


### __construct

Creates the object.

```php
public __construct(\Sabre\DAVACL\PrincipalBackend\BackendInterface $principalBackend, array $principalInfo): mixed
```

Note that you MUST supply the parent principal information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalBackend` | **\Sabre\DAVACL\PrincipalBackend\BackendInterface** |  |
| `$principalInfo` | **array** |  |





***

### getName

Returns this principals name.

```php
public getName(): string
```












***

### getLastModified

Returns the last modification time.

```php
public getLastModified(): int|null
```












***

### delete

Deletes the current node.

```php
public delete(): mixed
```











**Throws:**

- [`Forbidden`](../../DAV/Exception/Forbidden.md)



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

- [`Forbidden`](../../DAV/Exception/Forbidden.md)



***

### getAlternateUriSet

Returns a list of alternative urls for a principal.

```php
public getAlternateUriSet(): array
```

This can for example be an email address, or ldap url.










***

### getPrincipalUrl

Returns the full principal url.

```php
public getPrincipalUrl(): string
```












***

### getGroupMemberSet

Returns the list of group members.

```php
public getGroupMemberSet(): array
```

If this principal is a group, this function should return
all member principal uri's for the group.










***

### getGroupMembership

Returns the list of groups this principal is member of.

```php
public getGroupMembership(): array
```

If this principal is a member of a (list of) groups, this function
should return a list of principal uri's for it's members.










***

### setGroupMemberSet

Sets a list of group members.

```php
public setGroupMemberSet(array $principals): mixed
```

If this principal is a group, this method sets all the group members.
The list of members is always overwritten, never appended to.

This method should throw an exception if the members could not be set.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principals` | **array** |  |





***

### getDisplayName

Returns the displayname.

```php
public getDisplayName(): string
```

This should be a human readable name for the principal.
If none is available, return the nodename.










***


***
> Automatically generated on 2025-03-18
