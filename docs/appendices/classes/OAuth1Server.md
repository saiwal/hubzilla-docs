
# OAuth1Server





* Full name: `\OAuth1Server`



## Properties


### timestamp_threshold



```php
protected $timestamp_threshold
```






***

### version



```php
protected $version
```






***

### signature_methods



```php
protected $signature_methods
```






***

### data_store



```php
protected $data_store
```






***

## Methods


### __construct



```php
public __construct(mixed $data_store): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data_store` | **mixed** |  |





***

### add_signature_method



```php
public add_signature_method(mixed $signature_method): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$signature_method` | **mixed** |  |





***

### fetch_request_token

process a request_token request
returns the request token on success

```php
public fetch_request_token(mixed& $request): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### fetch_access_token

process an access_token request
returns the access token on success

```php
public fetch_access_token(mixed& $request): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### verify_request

verify an api call, checks all the parameters

```php
public verify_request(mixed& $request): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### get_version

version 1

```php
private get_version(mixed& $request): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### get_signature_method

figure out the signature with some defaults

```php
private get_signature_method(mixed& $request): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### get_consumer

try to find the consumer for the provided request's consumer key

```php
private get_consumer(mixed& $request): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |





***

### get_token

try to find the token for the provided request's token key

```php
private get_token(mixed& $request, mixed $consumer, mixed $token_type = &quot;access&quot;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$token_type` | **mixed** |  |





***

### check_signature

all-in-one function to check the signature on a request
should guess the signature method appropriately

```php
private check_signature(mixed& $request, mixed $consumer, mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** |  |
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |





***

### check_timestamp

check that the timestamp is new enough

```php
private check_timestamp(mixed $timestamp): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timestamp` | **mixed** |  |





***

### check_nonce

check that the nonce is not repeated

```php
private check_nonce(mixed $consumer, mixed $token, mixed $nonce, mixed $timestamp): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$consumer` | **mixed** |  |
| `$token` | **mixed** |  |
| `$nonce` | **mixed** |  |
| `$timestamp` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
