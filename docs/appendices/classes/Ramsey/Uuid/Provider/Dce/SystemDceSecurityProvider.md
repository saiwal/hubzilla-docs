
# SystemDceSecurityProvider

SystemDceSecurityProvider retrieves the user or group identifiers from the system



* Full name: `\Ramsey\Uuid\Provider\Dce\SystemDceSecurityProvider`
* This class implements:
[`\Ramsey\Uuid\Provider\DceSecurityProviderInterface`](../DceSecurityProviderInterface.md)




## Methods


### getUid

Returns a user identifier for the system

```php
public getUid(): \Ramsey\Uuid\Type\Integer
```











**Throws:**
<p>if unable to get a user identifier</p>

- [`DceSecurityException`](../../Exception/DceSecurityException.md)



***

### getGid

Returns a group identifier for the system

```php
public getGid(): \Ramsey\Uuid\Type\Integer
```











**Throws:**
<p>if unable to get a group identifier</p>

- [`DceSecurityException`](../../Exception/DceSecurityException.md)



***

### getSystemUid

Returns the UID from the system

```php
private getSystemUid(): string
```












***

### getSystemGid

Returns the GID from the system

```php
private getSystemGid(): string
```












***

### hasShellExec

Returns true if shell_exec() is available for use

```php
private hasShellExec(): bool
```












***

### getOs

Returns the PHP_OS string

```php
private getOs(): string
```












***

### getWindowsUid

Returns the user identifier for a user on a Windows system

```php
private getWindowsUid(): string
```

Windows does not have the same concept as an effective POSIX UID for the
running script. Instead, each user is uniquely identified by an SID
(security identifier). The SID includes three 32-bit unsigned integers
that make up a unique domain identifier, followed by an RID (relative
identifier) that we will use as the UID. The primary caveat is that this
UID may not be unique to the system, since it is, instead, unique to the
domain.










**See Also:**

* https://www.lifewire.com/what-is-an-sid-number-2626005 - What Is an SID Number?* https://bit.ly/30vE7NM - Well-known SID Structures* https://bit.ly/2FWcYKJ - Well-known security identifiers in Windows operating systems* https://www.windows-commandline.com/get-sid-of-user/ - Get SID of user

***

### getWindowsGid

Returns a group identifier for a user on a Windows system

```php
private getWindowsGid(): string
```

Since Windows does not have the same concept as an effective POSIX GID
for the running script, we will get the local group memberships for the
user running the script. Then, we will get the SID (security identifier)
for the first group that appears in that list. Finally, we will return
the RID (relative identifier) for the group and use that as the GID.










**See Also:**

* https://www.windows-commandline.com/list-of-user-groups-command-line/ - List of user groups command line

***


***
> Automatically generated on 2025-03-18
