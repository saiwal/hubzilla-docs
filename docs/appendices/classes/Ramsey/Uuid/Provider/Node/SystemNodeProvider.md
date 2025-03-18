
# SystemNodeProvider

SystemNodeProvider retrieves the system node ID, if possible

The system node ID, or host ID, is often the same as the MAC address for a
network interface on the host.

* Full name: `\Ramsey\Uuid\Provider\Node\SystemNodeProvider`
* This class implements:
[`\Ramsey\Uuid\Provider\NodeProviderInterface`](../NodeProviderInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`IFCONFIG_PATTERN`|private| |&#039;/[^:]([0-9a-f]{2}([:-])[0-9a-f]{2}(\2[0-9a-f]{2}){4})[^:]/i&#039;|
|`SYSFS_PATTERN`|private| |&#039;/^([0-9a-f]{2}:){5}[0-9a-f]{2}$/i&#039;|


## Methods


### getNode

Returns a node ID

```php
public getNode(): \Ramsey\Uuid\Type\Hexadecimal
```









**Return Value:**

The node ID as a hexadecimal string




***

### getNodeFromSystem

Returns the system node, if it can find it

```php
protected getNodeFromSystem(): string
```












***

### getIfconfig

Returns the network interface configuration for the system

```php
protected getIfconfig(): string
```












***

### getSysfs

Returns MAC address from the first system interface via the sysfs interface

```php
protected getSysfs(): string
```












***


***
> Automatically generated on 2025-03-18
