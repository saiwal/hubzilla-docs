***

# ZotOAuth1DataStore





* Full name: `\ZotOAuth1DataStore`
* Parent class: [`\OAuth1DataStore`](./OAuth1DataStore.md)




## Methods


### gen_token



```php
public gen_token(): mixed
```












***

### lookup_consumer



```php
public lookup_consumer(mixed $consumer_key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer_key` | **mixed** |  |





***

### lookup_token



```php
public lookup_token(mixed $consumer, mixed $token_type, mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$token_type` | **mixed** |  |
| `$token` | **mixed** |  |





***

### lookup_nonce



```php
public lookup_nonce(mixed $consumer, mixed $token, mixed $nonce, mixed $timestamp): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |
| `$nonce` | **mixed** |  |
| `$timestamp` | **mixed** |  |





***

### new_request_token



```php
public new_request_token(mixed $consumer, mixed $callback = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$callback` | **mixed** |  |





***

### new_access_token



```php
public new_access_token(mixed $token, mixed $consumer, mixed $verifier = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$verifier` | **mixed** |  |





***


## Inherited methods


### lookup_consumer



```php
public lookup_consumer(mixed $consumer_key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer_key` | **mixed** |  |





***

### lookup_token



```php
public lookup_token(mixed $consumer, mixed $token_type, mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$token_type` | **mixed** |  |
| `$token` | **mixed** |  |





***

### lookup_nonce



```php
public lookup_nonce(mixed $consumer, mixed $token, mixed $nonce, mixed $timestamp): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |
| `$nonce` | **mixed** |  |
| `$timestamp` | **mixed** |  |





***

### new_request_token



```php
public new_request_token(mixed $consumer, mixed $callback = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$callback` | **mixed** |  |





***

### new_access_token



```php
public new_access_token(mixed $token, mixed $consumer, mixed $verifier = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$verifier` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
