
# ISubscription

ISubscription.

Nodes implementing this interface represent calendar subscriptions.

The subscription node doesn't do much, other than returning and updating
subscription-related properties.

The following properties should be supported:

1. {DAV:}displayname
2. {http://apple.com/ns/ical/}refreshrate
3. {http://calendarserver.org/ns/}subscribed-strip-todos (omit if todos
   should not be stripped).
4. {http://calendarserver.org/ns/}subscribed-strip-alarms (omit if alarms
   should not be stripped).
5. {http://calendarserver.org/ns/}subscribed-strip-attachments (omit if
   attachments should not be stripped).
6. {http://calendarserver.org/ns/}source (Must be a
    Sabre\DAV\Property\Href).
7. {http://apple.com/ns/ical/}calendar-color
8. {http://apple.com/ns/ical/}calendar-order

It is recommended to support every property.

* Full name: `\Sabre\CalDAV\Subscriptions\ISubscription`
* Parent interfaces: [`\Sabre\DAV\ICollection`](../../DAV/ICollection.md), [`\Sabre\DAV\IProperties`](../../DAV/IProperties.md)




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
> Automatically generated on 2025-03-18
