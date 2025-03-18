
# EncryptionInterface





* Full name: `\OAuth2\Encryption\EncryptionInterface`



## Methods


### encode



```php
public encode(mixed $payload, mixed $key, null $algorithm = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$payload` | **mixed** |  |
| `$key` | **mixed** |  |
| `$algorithm` | **null** |  |





***

### decode



```php
public decode(mixed $payload, mixed $key, null $algorithm = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$payload` | **mixed** |  |
| `$key` | **mixed** |  |
| `$algorithm` | **null** |  |





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
