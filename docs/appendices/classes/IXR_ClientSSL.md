
# IXR_ClientSSL

Client for communicating with a XML-RPC Server over HTTPS.



* Full name: `\IXR_ClientSSL`
* Parent class: [`\IXR_Client`](./IXR_Client.md)



## Properties


### _certFile

Filename of the SSL Client Certificate

```php
public string $_certFile
```






***

### _caFile

Filename of the SSL CA Certificate

```php
public string $_caFile
```






***

### _keyFile

Filename of the SSL Client Private Key

```php
public string $_keyFile
```






***

### _passphrase

Passphrase to unlock the private key

```php
public string $_passphrase
```






***

## Methods


### __construct

Constructor

```php
public __construct(string $server, mixed $path = false, mixed $port = 443, mixed $timeout = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **string** | URL of the Server to connect to |
| `$path` | **mixed** |  |
| `$port` | **mixed** |  |
| `$timeout` | **mixed** |  |





***

### setCertificate

Set the client side certificates to communicate with the server.

```php
public setCertificate(string $certificateFile, string $keyFile, string $keyPhrase = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$certificateFile` | **string** | Filename of the client side certificate to use |
| `$keyFile` | **string** | Filename of the client side certificate&#039;s private key |
| `$keyPhrase` | **string** | Passphrase to unlock the private key |





***

### setCACertificate



```php
public setCACertificate(mixed $caFile): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$caFile` | **mixed** |  |





***

### setTimeOut

Sets the connection timeout (in seconds)

```php
public setTimeOut(int $newTimeOut): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$newTimeOut` | **int** | Timeout in seconds |





***

### getTimeOut

Returns the connection timeout (in seconds)

```php
public getTimeOut(): mixed
```












***

### query

Set the query to send to the XML-RPC Server

```php
public query(): mixed
```












***


## Inherited methods


### __construct



```php
public __construct(mixed $server, mixed $path = false, mixed $port = 80, mixed $timeout = 15): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **mixed** |  |
| `$path` | **mixed** |  |
| `$port` | **mixed** |  |
| `$timeout` | **mixed** |  |





***

### query



```php
public query(): mixed
```












***

### getResponse



```php
public getResponse(): mixed
```












***

### isError



```php
public isError(): mixed
```












***

### getErrorCode



```php
public getErrorCode(): mixed
```












***

### getErrorMessage



```php
public getErrorMessage(): mixed
```












***


***
> Automatically generated on 2025-03-18
