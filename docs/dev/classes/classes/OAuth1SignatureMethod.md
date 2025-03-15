***

# OAuth1SignatureMethod

A class for implementing a Signature Method
See section 9 ("Signing Requests") in the spec



* Full name: `\OAuth1SignatureMethod`
* This class is an **Abstract class**




## Methods


### get_name

Needs to return the name of the Signature Method (ie HMAC-SHA1)

```php
public get_name(): string
```




* This method is **abstract**.







***

### build_signature

Build up the signature
NOTE: The output of this function MUST NOT be urlencoded.

```php
public build_signature(\OAuth1Request $request, \OAuth1Consumer $consumer, \OAuth1Token $token): string
```

the encoding is handled in OAuth1Request when the final
request is serialized


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth1Request** |  |
| `$consumer` | **\OAuth1Consumer** |  |
| `$token` | **\OAuth1Token** |  |





***

### check_signature

Verifies that a given signature is correct

```php
public check_signature(\OAuth1Request $request, \OAuth1Consumer $consumer, \OAuth1Token $token, string $signature): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\OAuth1Request** |  |
| `$consumer` | **\OAuth1Consumer** |  |
| `$token` | **\OAuth1Token** |  |
| `$signature` | **string** |  |





***


***
> Automatically generated on 2025-03-15
