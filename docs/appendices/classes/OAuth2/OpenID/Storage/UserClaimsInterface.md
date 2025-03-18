
# UserClaimsInterface

Implement this interface to specify where the OAuth2 Server
should retrieve user claims for the OpenID Connect id_token.



* Full name: `\OAuth2\OpenID\Storage\UserClaimsInterface`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`VALID_CLAIMS`|public| |&#039;profile email address phone&#039;|
|`PROFILE_CLAIM_VALUES`|public| |&#039;name family_name given_name middle_name nickname preferred_username profile picture website gender birthdate zoneinfo locale updated_at&#039;|
|`EMAIL_CLAIM_VALUES`|public| |&#039;email email_verified&#039;|
|`ADDRESS_CLAIM_VALUES`|public| |&#039;formatted street_address locality region postal_code country&#039;|
|`PHONE_CLAIM_VALUES`|public| |&#039;phone_number phone_number_verified&#039;|

## Methods


### getUserClaims

Return claims about the provided user id.

```php
public getUserClaims(mixed $user_id, string $scope): array
```

Groups of claims are returned based on the requested scopes. No group
is required, and no claim is required.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$user_id` | **mixed** | - The id of the user for which claims should be returned. |
| `$scope` | **string** | - The requested scope.<br />Scopes with matching claims: profile, email, address, phone. |


**Return Value:**

- An array in the claim => value format.




**See Also:**

* http://openid.net/specs/openid-connect-core-1_0.html#ScopeClaims - 

***


***
> Automatically generated on 2025-03-18
