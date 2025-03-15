***

# PDO

The Lock manager allows you to handle all file-locks centrally.

This Lock Manager stores all its data in a database. You must pass a PDO
connection object in the constructor.

* Full name: `\Sabre\DAV\Locks\Backend\PDO`
* Parent class: [`\Sabre\DAV\Locks\Backend\AbstractBackend`](./AbstractBackend.md)



## Properties


### tableName

The PDO tablename this backend uses.

```php
public string $tableName
```






***

### pdo

The PDO connection object.

```php
protected \Sabre\DAV\Locks\Backend\pdo $pdo
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### getLocks

Returns a list of Sabre\DAV\Locks\LockInfo objects.

```php
public getLocks(string $uri, bool $returnChildLocks): array
```

This method should return all the locks for a particular uri, including
locks that might be set on a parent uri.

If returnChildLocks is set to true, this method should also look for
any locks in the subtree of the uri for locks.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$returnChildLocks` | **bool** |  |





***

### lock

Locks a uri.

```php
public lock(string $uri, \Sabre\DAV\Locks\LockInfo $lockInfo): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$lockInfo` | **\Sabre\DAV\Locks\LockInfo** |  |





***

### unlock

Removes a lock from a uri.

```php
public unlock(string $uri, \Sabre\DAV\Locks\LockInfo $lockInfo): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$lockInfo` | **\Sabre\DAV\Locks\LockInfo** |  |





***


***
> Automatically generated on 2025-03-15
