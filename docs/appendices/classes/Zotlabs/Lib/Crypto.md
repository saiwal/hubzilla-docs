
# Crypto





* Full name: `\Zotlabs\Lib\Crypto`



## Properties


### openssl_algorithms



```php
public static $openssl_algorithms
```



* This property is **static**.


***

## Methods


### methods



```php
public static methods(): mixed
```



* This method is **static**.








***

### signing_methods



```php
public static signing_methods(): mixed
```



* This method is **static**.








***

### new_keypair



```php
public static new_keypair(mixed $bits): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bits` | **mixed** |  |





***

### sign



```php
public static sign(mixed $data, mixed $key, mixed $alg = &#039;sha256&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$key` | **mixed** |  |
| `$alg` | **mixed** |  |





***

### verify



```php
public static verify(mixed $data, mixed $sig, mixed $key, mixed $alg = &#039;sha256&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$sig` | **mixed** |  |
| `$key` | **mixed** |  |
| `$alg` | **mixed** |  |





***

### encapsulate



```php
public static encapsulate(mixed $data, mixed $pubkey, mixed $alg): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$pubkey` | **mixed** |  |
| `$alg` | **mixed** |  |





***

### unencapsulate



```php
public static unencapsulate(mixed $data, mixed $prvkey): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$prvkey` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
