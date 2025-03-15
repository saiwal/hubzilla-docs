
# ISharedCalendar

This interface represents a Calendar that is shared by a different user.



* Full name: `\Sabre\CalDAV\ISharedCalendar`
* Parent interfaces: [`\Sabre\DAV\Sharing\ISharedNode`](../DAV/Sharing/ISharedNode.md)


## Methods


### setPublishStatus

Marks this calendar as published.

```php
public setPublishStatus(bool $value): mixed
```

Publishing a calendar should automatically create a read-only, public,
subscribable calendar.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **bool** |  |





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

### getShareAccess

Returns the 'access level' for the instance of this shared resource.

```php
public getShareAccess(): int
```

The value should be one of the Sabre\DAV\Sharing\Plugin::ACCESS_
constants.










***

### getShareResourceUri

This function must return a URI that uniquely identifies the shared
resource. This URI should be identical across instances, and is
also used in several other XML bodies to connect invites to
resources.

```php
public getShareResourceUri(): string
```

This may simply be a relative reference to the original shared instance,
but it could also be a urn. As long as it's a valid URI and unique.










***

### updateInvites

Updates the list of sharees.

```php
public updateInvites(\Sabre\DAV\Xml\Element\Sharee[] $sharees): mixed
```

Every item must be a Sharee object.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sharees` | **\Sabre\DAV\Xml\Element\Sharee[]** |  |





***

### getInvites

Returns the list of people whom this resource is shared with.

```php
public getInvites(): \Sabre\DAV\Xml\Element\Sharee[]
```

Every item in the returned array must be a Sharee object with
at least the following properties set:

* $href
* $shareAccess
* $inviteStatus

and optionally:

* $properties










***


***
> Automatically generated on 2025-03-15
