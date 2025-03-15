
# File

This Locks backend stores all locking information in a single file.

Note that this is not nearly as robust as a database. If you are considering
using this backend, keep in mind that the PDO backend can work with SqLite,
which is designed to be a good file-based database.

It literally solves the problem this class solves as well, but much better.

* Full name: `\Sabre\DAV\Locks\Backend\File`
* Parent class: [`\Sabre\DAV\Locks\Backend\AbstractBackend`](./AbstractBackend.md)



## Properties


### locksFile

The storage file.

```php
private string $locksFile
```






***

## Methods


### __construct

Constructor.

```php
public __construct(string $locksFile): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locksFile` | **string** | path to file |





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

### getData

Loads the lockdata from the filesystem.

```php
protected getData(): array
```












***

### putData

Saves the lockdata.

```php
protected putData(array $newData): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$newData` | **array** |  |





***


***
> Automatically generated on 2025-03-15
