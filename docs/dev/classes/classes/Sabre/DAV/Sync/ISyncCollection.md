
# ISyncCollection

If a class extends ISyncCollection, it supports WebDAV-sync.

You are responsible for maintaining a changelist for this collection. This
means that if any child nodes in this collection was created, modified or
deleted in any way, you should maintain an updated changelist.

* Full name: `\Sabre\DAV\Sync\ISyncCollection`
* Parent interfaces: [`\Sabre\DAV\ICollection`](../ICollection.md)


## Methods


### getSyncToken

This method returns the current sync-token for this collection.

```php
public getSyncToken(): string|null
```

This can be any string.

If null is returned from this function, the plugin assumes there's no
sync information available.










***

### getChanges

The getChanges method returns all the changes that have happened, since
the specified syncToken and the current collection.

```php
public getChanges(string $syncToken, int $syncLevel, int $limit = null): array|null
```

This function should return an array, such as the following:

[
  'syncToken' => 'The current synctoken',
  'added'   => [
     'new.txt',
  ],
  'modified'   => [
     'modified.txt',
  ],
  'deleted' => array(
     'foo.php.bak',
     'old.txt'
  )
];

The syncToken property should reflect the *current* syncToken of the
collection, as reported getSyncToken(). This is needed here too, to
ensure the operation is atomic.

If the syncToken is specified as null, this is an initial sync, and all
members should be reported.

The modified property is an array of nodenames that have changed since
the last token.

The deleted property is an array with nodenames, that have been deleted
from collection.

The second argument is basically the 'depth' of the report. If it's 1,
you only have to report changes that happened only directly in immediate
descendants. If it's 2, it should also include changes from the nodes
below the child collections. (grandchildren)

The third (optional) argument allows a client to specify how many
results should be returned at most. If the limit is not specified, it
should be treated as infinite.

If the limit (infinite or not) is higher than you're willing to return,
you should throw a Sabre\DAV\Exception\TooMuchMatches() exception.

If the syncToken is expired (due to data cleanup) or unknown, you must
return null.

The limit is 'suggestive'. You are free to ignore it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$syncToken` | **string** |  |
| `$syncLevel` | **int** |  |
| `$limit` | **int** |  |





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
