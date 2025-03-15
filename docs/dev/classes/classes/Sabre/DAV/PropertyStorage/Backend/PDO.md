***

# PDO

PropertyStorage PDO backend.

This backend class uses a PDO-enabled database to store webdav properties.
Both sqlite and mysql have been tested.

The database structure can be found in the examples/sql/ directory.

* Full name: `\Sabre\DAV\PropertyStorage\Backend\PDO`
* This class implements:
[`\Sabre\DAV\PropertyStorage\Backend\BackendInterface`](./BackendInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`VT_STRING`|public| |1|
|`VT_XML`|public| |2|
|`VT_OBJECT`|public| |3|

## Properties


### pdo

PDO.

```php
protected \PDO $pdo
```






***

### tableName

PDO table name we'll be using.

```php
public string $tableName
```






***

## Methods


### __construct

Creates the PDO property storage engine.

```php
public __construct(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### propFind

Fetches properties for a path.

```php
public propFind(string $path, \Sabre\DAV\PropFind $propFind): mixed
```

This method received a PropFind object, which contains all the
information about the properties that need to be fetched.

Usually you would just want to call 'get404Properties' on this object,
as this will give you the _exact_ list of properties that need to be
fetched, and haven't yet.

However, you can also support the 'allprops' property here. In that
case, you should check for $propFind->isAllProps().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propFind` | **\Sabre\DAV\PropFind** |  |





***

### propPatch

Updates properties for a path.

```php
public propPatch(string $path, \Sabre\DAV\PropPatch $propPatch): mixed
```

This method received a PropPatch object, which contains all the
information about the update.

Usually you would want to call 'handleRemaining' on this object, to get;
a list of all properties that need to be stored.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### delete

This method is called after a node is deleted.

```php
public delete(string $path): mixed
```

This allows a backend to clean up all associated properties.

The delete method will get called once for the deletion of an entire
tree.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### move

This method is called after a successful MOVE.

```php
public move(string $source, string $destination): mixed
```

This should be used to migrate all properties from one path to another.
Note that entire collections may be moved, so ensure that all properties
for children are also moved along.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |
| `$destination` | **string** |  |





***


***
> Automatically generated on 2025-03-15
