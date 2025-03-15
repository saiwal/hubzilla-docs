
# OAuth1SignatureMethod_PLAINTEXT

The PLAINTEXT method does not provide any security protection and SHOULD only be used
over a secure channel such as HTTPS. It does not use the Signature Base String.

- Chapter 9.4 ("PLAINTEXT")

* Full name: `\OAuth1SignatureMethod_PLAINTEXT`
* Parent class: [`\OAuth1SignatureMethod`](./OAuth1SignatureMethod.md)




## Methods


### get_name

Needs to return the name of the Signature Method (ie HMAC-SHA1)

```php
public get_name(): string
```












***

### build_signature

oauth_signature is set to the concatenated encoded values of the Consumer Secret and
Token Secret, separated by a '&' character (ASCII code 38), even if either secret is
empty. The result MUST be encoded again.

```php
public build_signature(mixed $request, mixed $consumer, mixed $token): string
```

- Chapter 9.4.1 ("Generating Signatures")

Please note that the second encoding MUST NOT happen in the SignatureMethod, as
OAuth1Request handles this!






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |





***


## Inherited methods


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
