
# Jwt





* Full name: `\OAuth2\Encryption\Jwt`
* This class implements:
[`\OAuth2\Encryption\EncryptionInterface`](./EncryptionInterface.md)

**See Also:**

* https://github.com/F21/jwt - 




## Methods


### encode



```php
public encode(mixed $payload, mixed $key, string $algo = &#039;HS256&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$payload` | **mixed** |  |
| `$key` | **mixed** |  |
| `$algo` | **string** |  |





***

### decode



```php
public decode(string $jwt, null $key = null, array|bool $allowedAlgorithms = true): bool|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$jwt` | **string** |  |
| `$key` | **null** |  |
| `$allowedAlgorithms` | **array&#124;bool** |  |





***

### verifySignature



```php
private verifySignature(mixed $signature, mixed $input, mixed $key, string $algo = &#039;HS256&#039;): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$signature` | **mixed** |  |
| `$input` | **mixed** |  |
| `$key` | **mixed** |  |
| `$algo` | **string** |  |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### sign



```php
private sign(mixed $input, mixed $key, string $algo = &#039;HS256&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$key` | **mixed** |  |
| `$algo` | **string** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### generateRSASignature



```php
private generateRSASignature(mixed $input, mixed $key, string $algo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$key` | **mixed** |  |
| `$algo` | **string** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### urlSafeB64Encode



```php
public urlSafeB64Encode(string $data): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### urlSafeB64Decode



```php
public urlSafeB64Decode(string $b64): mixed|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$b64` | **string** |  |





***

### generateJwtHeader

Override to create a custom header

```php
protected generateJwtHeader(mixed $payload, mixed $algorithm): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$payload` | **mixed** |  |
| `$algorithm` | **mixed** |  |





***

### hash_equals



```php
protected hash_equals(string $a, string $b): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **string** |  |
| `$b` | **string** |  |





***


***
> Automatically generated on 2025-03-15
