
# ClientInterface

Implement this interface to specify where the OAuth2 Server
should retrieve client information



* Full name: `\OAuth2\Storage\ClientInterface`



## Methods


### getClientDetails

Get client details corresponding client_id.

```php
public getClientDetails(mixed $client_id): array
```

OAuth says we should store request URIs for each registered client.
Implement this function to grab the stored URI for a given client id.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be check with. |


**Return Value:**


Client details. The only mandatory key in the array is "redirect_uri".
This function MUST return FALSE if the given client does not exist or is
invalid. "redirect_uri" can be space-delimited to allow for multiple valid uris.
<code>
return array(
"redirect_uri" => REDIRECT_URI,      // REQUIRED redirect_uri registered for the client
"client_id"    => CLIENT_ID,         // OPTIONAL the client id
"grant_types"  => GRANT_TYPES,       // OPTIONAL an array of restricted grant types
"user_id"      => USER_ID,           // OPTIONAL the user identifier associated with this client
"scope"        => SCOPE,             // OPTIONAL the scopes allowed for this client
);
</code>




***

### getClientScope

Get the scope associated with this client

```php
public getClientScope(mixed $client_id): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |


**Return Value:**

the space-delineated scope list for the specified client_id




***

### checkRestrictedGrantType

Check restricted grant types of corresponding client identifier.

```php
public checkRestrictedGrantType(mixed $client_id, mixed $grant_type): true
```

If you want to restrict clients to certain grant types, override this
function.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** | <br />Client identifier to be check with. |
| `$grant_type` | **mixed** | <br />Grant type to be check with |


**Return Value:**

if the grant type is supported by this client identifier, and
FALSE if it isn't.




***


***
> Automatically generated on 2025-03-15
