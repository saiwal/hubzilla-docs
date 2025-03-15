***

# PublicKeyInterface

Implement this interface to specify where the OAuth2 Server
should get public/private key information



* Full name: `\OAuth2\Storage\PublicKeyInterface`



## Methods


### getPublicKey



```php
public getPublicKey(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getPrivateKey



```php
public getPrivateKey(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### getEncryptionAlgorithm



```php
public getEncryptionAlgorithm(mixed $client_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
