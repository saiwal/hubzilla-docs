
# PDOBasicAuth

This is an authentication backend that uses a database to manage passwords.



* Full name: `\Sabre\DAV\Auth\Backend\PDOBasicAuth`
* Parent class: [`\Sabre\DAV\Auth\Backend\AbstractBasic`](./AbstractBasic.md)



## Properties


### pdo

Reference to PDO connection.

```php
protected \Sabre\DAV\Auth\Backend\PDO $pdo
```






***

### tableName

PDO table name we'll be using.

```php
protected string $tableName
```






***

### digestColumn

PDO digest column name we'll be using
(i.e. digest, password, password_hash).

```php
protected string $digestColumn
```






***

### uuidColumn

PDO uuid(unique user identifier) column name we'll be using
(i.e. username, email).

```php
protected string $uuidColumn
```






***

### digestPrefix

Digest prefix:
if the backend you are using for is prefixing
your password hashes set this option to your prefix to
cut it off before verfiying.

```php
protected string $digestPrefix
```






***

## Methods


### __construct

Creates the backend object.

```php
public __construct(\PDO $pdo, array $options = []): mixed
```

If the filename argument is passed in, it will parse out the specified file fist.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |
| `$options` | **array** |  |





***

### validateUserPass

Validates a username and password.

```php
public validateUserPass(string $username, string $password): bool
```

This method should return true or false depending on if login
succeeded.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |





***


## Inherited methods


### validateUserPass

Validates a username and password.

```php
protected validateUserPass(string $username, string $password): bool
```

This method should return true or false depending on if login
succeeded.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |





***

### setRealm

Sets the authentication realm for this backend.

```php
public setRealm(string $realm): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **string** |  |





***

### check

When this method is called, the backend must check if authentication was
successful.

```php
public check(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): array
```

The returned value must be one of the following

[true, "principals/username"]
[false, "reason for failure"]

If authentication was successful, it's expected that the authentication
backend returns a so-called principal url.

Examples of a principal url:

principals/admin
principals/user1
principals/users/joe
principals/uid/123457

If you don't use WebDAV ACL (RFC3744) we recommend that you simply
return a string such as:

principals/users/[username]






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### challenge

This method is called when a user could not be authenticated, and
authentication was required for the current request.

```php
public challenge(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

This gives you the opportunity to set authentication headers. The 401
status code will already be set.

In this case of Basic Auth, this would for example mean that the
following header needs to be set:

$response->addHeader('WWW-Authenticate', 'Basic realm=SabreDAV');

Keep in mind that in the case of multiple authentication backends, other
WWW-Authenticate headers may already have been set, and you'll want to
append your own WWW-Authenticate header instead of overwriting the
existing one.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***


***
> Automatically generated on 2025-03-18
