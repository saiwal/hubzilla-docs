
# AWS

HTTP AWS Authentication handler.

Use this class to leverage amazon's AWS authentication header

* Full name: `\Sabre\HTTP\Auth\AWS`
* Parent class: [`\Sabre\HTTP\Auth\AbstractAuth`](./AbstractAuth.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`ERR_NOAWSHEADER`|public| |1|
|`ERR_MD5CHECKSUMWRONG`|public| |2|
|`ERR_INVALIDDATEFORMAT`|public| |3|
|`ERR_REQUESTTIMESKEWED`|public| |4|
|`ERR_INVALIDSIGNATURE`|public| |5|

## Properties


### signature

The signature supplied by the HTTP client.

```php
private string $signature
```






***

### accessKey

The accesskey supplied by the HTTP client.

```php
private string $accessKey
```






***

### errorCode

An error code, if any.

```php
public int $errorCode
```

This value will be filled with one of the ERR_* constants




***

## Methods


### init

Gathers all information from the headers.

```php
public init(): bool
```

This method needs to be called prior to anything else.










***

### getAccessKey

Returns the username for the request.

```php
public getAccessKey(): string
```












***

### validate

Validates the signature based on the secretKey.

```php
public validate(string $secretKey): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$secretKey` | **string** |  |





***

### requireLogin

Returns an HTTP 401 header, forcing login.

```php
public requireLogin(): mixed
```

This should be called when username and password are incorrect, or not supplied at all










***

### validateRFC2616Date

Makes sure the supplied value is a valid RFC2616 date.

```php
protected validateRFC2616Date(string $dateHeader): bool
```

If we would just use strtotime to get a valid timestamp, we have no way of checking if a
user just supplied the word 'now' for the date header.

This function also makes sure the Date header is within 15 minutes of the operating
system date, to prevent replay attacks.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dateHeader` | **string** |  |





***

### getAmzHeaders

Returns a list of AMZ headers.

```php
protected getAmzHeaders(): string
```












***

### hmacsha1

Generates an HMAC-SHA1 signature.

```php
private hmacsha1(string $key, string $message): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$message` | **string** |  |





***


## Inherited methods


### __construct

Creates the object.

```php
public __construct(string $realm, \Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **string** |  |
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### requireLogin

This method sends the needed HTTP header and status code (401) to force
the user to login.

```php
public requireLogin(): mixed
```




* This method is **abstract**.







***

### getRealm

Returns the HTTP realm.

```php
public getRealm(): string
```












***


***
> Automatically generated on 2025-03-18
