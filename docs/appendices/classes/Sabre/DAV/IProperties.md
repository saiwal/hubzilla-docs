
# IProperties

IProperties interface.

Implement this interface to support custom WebDAV properties requested and sent from clients.

* Full name: `\Sabre\DAV\IProperties`
* Parent interfaces: [`\Sabre\DAV\INode`](./INode.md)


## Methods


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

### getProperties

Returns a list of properties for this nodes.

```php
public getProperties(array $properties): array
```

The properties list is a list of propertynames the client requested,
encoded in clark-notation {xmlnamespace}tagname

If the array is empty, it means 'all properties' were requested.

Note that it's fine to liberally give properties back, instead of
conforming to the list of requested properties.
The Server class will filter out the extra.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **array** |  |





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


***
> Automatically generated on 2025-03-18
