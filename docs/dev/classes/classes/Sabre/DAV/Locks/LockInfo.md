***

# LockInfo

LockInfo class.

An object of the LockInfo class holds all the information relevant to a
single lock.

* Full name: `\Sabre\DAV\Locks\LockInfo`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`SHARED`|public| |1|
|`EXCLUSIVE`|public| |2|
|`TIMEOUT_INFINITE`|public| |-1|

## Properties


### owner

The owner of the lock.

```php
public string $owner
```






***

### token

The locktoken.

```php
public string $token
```






***

### timeout

How long till the lock is expiring.

```php
public int $timeout
```






***

### created

UNIX Timestamp of when this lock was created.

```php
public int $created
```






***

### scope

Exclusive or shared lock.

```php
public int $scope
```






***

### depth

Depth of lock, can be 0 or Sabre\DAV\Server::DEPTH_INFINITY.

```php
public $depth
```






***

### uri

The uri this lock locks.

```php
public mixed $uri
```

TODO: This value is not always set




***



***
> Automatically generated on 2025-03-15
