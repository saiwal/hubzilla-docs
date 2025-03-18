
# FirebaseJwt

Bridge file to use the firebase/php-jwt package for JWT encoding and decoding.



* Full name: `\OAuth2\Encryption\FirebaseJwt`
* This class implements:
[`\OAuth2\Encryption\EncryptionInterface`](./EncryptionInterface.md)




## Methods


### __construct



```php
public __construct(): mixed
```












***

### encode



```php
public encode(mixed $payload, mixed $key, mixed $alg = &#039;HS256&#039;, mixed $keyId = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$payload` | **mixed** |  |
| `$key` | **mixed** |  |
| `$alg` | **mixed** |  |
| `$keyId` | **mixed** |  |





***

### decode



```php
public decode(mixed $jwt, mixed $key = null, mixed $allowedAlgorithms = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$jwt` | **mixed** |  |
| `$key` | **mixed** |  |
| `$allowedAlgorithms` | **mixed** |  |





***

### urlSafeB64Encode



```php
public urlSafeB64Encode(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### urlSafeB64Decode



```php
public urlSafeB64Decode(mixed $b64): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$b64` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
