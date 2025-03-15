
# OAuth1SignatureMethod_RSA_SHA1

The RSA-SHA1 signature method uses the RSASSA-PKCS1-v1_5 signature algorithm as defined in
[RFC3447] section 8.2 (more simply known as PKCS#1), using SHA-1 as the hash function for
EMSA-PKCS1-v1_5. It is assumed that the Consumer has provided its RSA public key in a
verified way to the Service Provider, in a manner which is beyond the scope of this
specification.

- Chapter 9.3 ("RSA-SHA1")

* Full name: `\OAuth1SignatureMethod_RSA_SHA1`
* Parent class: [`\OAuth1SignatureMethod`](./OAuth1SignatureMethod.md)
* This class is an **Abstract class**




## Methods


### get_name

Needs to return the name of the Signature Method (ie HMAC-SHA1)

```php
public get_name(): string
```












***

### fetch_public_cert



```php
protected fetch_public_cert(mixed& $request): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### fetch_private_cert



```php
protected fetch_private_cert(mixed& $request): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### build_signature

Build up the signature
NOTE: The output of this function MUST NOT be urlencoded.

```php
public build_signature(mixed $request, mixed $consumer, mixed $token): string
```

the encoding is handled in OAuth1Request when the final
request is serialized






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |





***

### check_signature

Verifies that a given signature is correct

```php
public check_signature(mixed $request, mixed $consumer, mixed $token, mixed $signature): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |
| `$signature` | **mixed** |  |





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
