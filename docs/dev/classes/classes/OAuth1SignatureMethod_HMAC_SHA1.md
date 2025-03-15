***

# OAuth1SignatureMethod_HMAC_SHA1

The HMAC-SHA1 signature method uses the HMAC-SHA1 signature algorithm as defined in [RFC2104]
where the Signature Base String is the text and the key is the concatenated values (each first
encoded per Parameter Encoding) of the Consumer Secret and Token Secret, separated by an '&'
character (ASCII code 38) even if empty.

- Chapter 9.2 ("HMAC-SHA1")

* Full name: `\OAuth1SignatureMethod_HMAC_SHA1`
* Parent class: [`\OAuth1SignatureMethod`](./OAuth1SignatureMethod.md)




## Methods


### get_name

Needs to return the name of the Signature Method (ie HMAC-SHA1)

```php
public get_name(): string
```












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
