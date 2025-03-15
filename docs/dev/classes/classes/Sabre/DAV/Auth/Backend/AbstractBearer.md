***

# AbstractBearer

HTTP Bearer authentication backend class.

This class can be used by authentication objects wishing to use HTTP Bearer
Most of the digest logic is handled, implementors just need to worry about
the validateBearerToken method.

* Full name: `\Sabre\DAV\Auth\Backend\AbstractBearer`
* This class implements:
[`\Sabre\DAV\Auth\Backend\BackendInterface`](./BackendInterface.md)
* This class is an **Abstract class**



## Properties


### realm

Authentication Realm.

```php
protected string $realm
```

The realm is often displayed by browser clients when showing the
authentication dialog.




***

## Methods


### validateBearerToken

Validates a Bearer token.

```php
protected validateBearerToken(string $bearerToken): string|false
```

This method should return the full principal url, or false if the
token was incorrect.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bearerToken` | **string** |  |





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

In this case of Bearer Auth, this would for example mean that the
following header needs to be set:

$response->addHeader('WWW-Authenticate', 'Bearer realm=SabreDAV');

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
> Automatically generated on 2025-03-15
