
# JwtBearerInterface

Implement this interface to specify where the OAuth2 Server
should get the JWT key for clients



* Full name: `\OAuth2\Storage\JwtBearerInterface`



## Methods


### getClientKey

Get the public key associated with a client_id

```php
public getClientKey(mixed $client_id, mixed $subject): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be checked with. |
| `$subject` | **mixed** |  |


**Return Value:**

Return the public key for the client_id if it exists, and MUST return FALSE if it doesn't.




***

### getJti

Get a jti (JSON token identifier) by matching against the client_id, subject, audience and expiration.

```php
public getJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expiration, mixed $jti): \OAuth2\Storage\An
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to match. |
| `$subject` | **mixed** | <br />The subject to match. |
| `$audience` | **mixed** | <br />The audience to match. |
| `$expiration` | **mixed** | <br />The expiration of the jti. |
| `$jti` | **mixed** | <br />The jti to match. |


**Return Value:**

associative array as below, and return NULL if the jti does not exist.
- issuer: Stored client identifier.
- subject: Stored subject.
- audience: Stored audience.
- expires: Stored expiration in unix timestamp.
- jti: The stored jti.




***

### setJti

Store a used jti so that we can check against it to prevent replay attacks.

```php
public setJti(mixed $client_id, mixed $subject, mixed $audience, mixed $expiration, mixed $jti): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to insert. |
| `$subject` | **mixed** | <br />The subject to insert. |
| `$audience` | **mixed** | <br />The audience to insert. |
| `$expiration` | **mixed** | <br />The expiration of the jti. |
| `$jti` | **mixed** | <br />The jti to insert. |





***


***
> Automatically generated on 2025-03-15
