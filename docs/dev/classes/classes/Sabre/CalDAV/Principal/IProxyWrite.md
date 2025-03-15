
# IProxyWrite

ProxyWrite principal interface.

Any principal node implementing this interface will be picked up as a 'proxy
principal group'.

* Full name: `\Sabre\CalDAV\Principal\IProxyWrite`
* Parent interfaces: [`\Sabre\DAVACL\IPrincipal`](../../DAVACL/IPrincipal.md)




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
> Automatically generated on 2025-03-15
