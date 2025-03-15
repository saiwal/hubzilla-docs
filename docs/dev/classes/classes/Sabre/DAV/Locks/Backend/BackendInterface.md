***

# BackendInterface

If you are defining your own Locks backend, you must implement this
interface.



* Full name: `\Sabre\DAV\Locks\Backend\BackendInterface`



## Methods


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
