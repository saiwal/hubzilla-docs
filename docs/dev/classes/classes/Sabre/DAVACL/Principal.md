
# Principal

Principal class.

This class is a representation of a simple principal

Many WebDAV specs require a user to show up in the directory
structure.

This principal also has basic ACL settings, only allowing the principal
access it's own principal.

* Full name: `\Sabre\DAVACL\Principal`
* Parent class: [`\Sabre\DAV\Node`](../DAV/Node.md)
* This class implements:
[`\Sabre\DAVACL\IPrincipal`](./IPrincipal.md), [`\Sabre\DAV\IProperties`](../DAV/IProperties.md), [`\Sabre\DAVACL\IACL`](./IACL.md)



## Properties


### principalProperties

Struct with principal information.

```php
protected array $principalProperties
```






***

### principalBackend

Principal backend.

```php
protected \Sabre\DAVACL\PrincipalBackend\BackendInterface $principalBackend
```






***

## Methods


### __construct

Creates the principal object.

```php
public __construct(\Sabre\DAVACL\PrincipalBackend\BackendInterface $principalBackend, array $principalProperties = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalBackend` | **\Sabre\DAVACL\PrincipalBackend\BackendInterface** |  |
| `$principalProperties` | **array** |  |





***

### getPrincipalUrl

Returns the full principal url.

```php
public getPrincipalUrl(): string
```












***

### getAlternateUriSet

Returns a list of alternative urls for a principal.

```php
public getAlternateUriSet(): array
```

This can for example be an email address, or ldap url.










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
public setGroupMemberSet(array $groupMembers): mixed
```

If this principal is a group, this method sets all the group members.
The list of members is always overwritten, never appended to.

This method should throw an exception if the members could not be set.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$groupMembers` | **array** |  |





***

### getName

Returns this principals name.

```php
public getName(): string
```












***

### getDisplayName

Returns the name of the user.

```php
public getDisplayName(): string
```












***

### getProperties

Returns a list of properties.

```php
public getProperties(array $requestedProperties): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$requestedProperties` | **array** |  |





***

### propPatch

Updates properties on this node.

```php
public propPatch(\Sabre\DAV\PropPatch $propPatch): mixed
```

This method received a PropPatch object, which contains all the
information about the update.

To update specific properties, call the 'handle' method on this object.
Read the PropPatch documentation for more information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### getOwner

Returns the owner principal.

```php
public getOwner(): string|null
```

This must be a url to a principal, or null if there's no owner










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

### getOwner

Returns the owner principal.

```php
public getOwner(): string|null
```

This must be a url to a principal, or null if there's no owner










***

### getGroup

Returns a group principal.

```php
public getGroup(): string|null
```

This must be a url to a principal, or null if there's no owner










***

### getACL

Returns a list of ACE's for this node.

```php
public getACL(): array
```

Each ACE has the following properties:
* 'privilege', a string such as {DAV:}read or {DAV:}write. These are
  currently the only supported privileges
* 'principal', a url to the principal who owns the node
* 'protected' (optional), indicating that this ACE is not allowed to
   be updated.










***

### setACL

Updates the ACL.

```php
public setACL(array $acl): mixed
```

This method will receive a list of new ACE's as an array argument.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$acl` | **array** |  |





***

### getSupportedPrivilegeSet

Returns the list of supported privileges for this node.

```php
public getSupportedPrivilegeSet(): array|null
```

The returned data structure is a list of nested privileges.
See Sabre\DAVACL\Plugin::getDefaultSupportedPrivilegeSet for a simple
standard structure.

If null is returned from this method, the default privilege set is used,
which is fine for most common usecases.










***


***
> Automatically generated on 2025-03-15
