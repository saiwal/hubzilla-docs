***

# AbstractDigest

HTTP Digest authentication backend class.

This class can be used by authentication objects wishing to use HTTP Digest
Most of the digest logic is handled, implementors just need to worry about
the getDigestHash method

* Full name: `\Sabre\DAV\Auth\Backend\AbstractDigest`
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

### principalPrefix

This is the prefix that will be used to generate principal urls.

```php
protected string $principalPrefix
```






***

## Methods


### setRealm

Sets the authentication realm for this backend.

```php
public setRealm(string $realm): mixed
```

Be aware that for Digest authentication, the realm influences the digest
hash. Choose the realm wisely, because if you change it later, all the
existing hashes will break and nobody can authenticate.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **string** |  |





***

### getDigestHash

Returns a users digest hash based on the username and realm.

```php
public getDigestHash(string $realm, string $username): string|null
```

If the user was not known, null must be returned.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **string** |  |
| `$username` | **string** |  |





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
> Automatically generated on 2025-03-15
