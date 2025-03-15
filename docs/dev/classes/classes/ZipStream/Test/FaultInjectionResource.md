
# FaultInjectionResource





* Full name: `\ZipStream\Test\FaultInjectionResource`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`NAME`|public| |&#039;zipstream-php-test-broken-resource&#039;|

## Properties


### context



```php
public resource $context
```






***

### injectFaults



```php
private array $injectFaults
```






***

### mode



```php
private string $mode
```






***

## Methods


### getResource



```php
public static getResource(array $injectFaults): resource
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$injectFaults` | **array** |  |





***

### stream_open



```php
public stream_open(string $path, string $mode, int $options, string& $opened_path = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$mode` | **string** |  |
| `$options` | **int** |  |
| `$opened_path` | **string** |  |





***

### stream_write



```php
public stream_write(string $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### stream_eof



```php
public stream_eof(): mixed
```












***

### stream_seek



```php
public stream_seek(int $offset, int $whence): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |
| `$whence` | **int** |  |





***

### stream_tell



```php
public stream_tell(): int
```












***

### register



```php
public static register(): void
```



* This method is **static**.








***

### stream_stat



```php
public stream_stat(): array
```












***

### url_stat



```php
public url_stat(string $path, int $flags): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$flags` | **int** |  |





***

### createStreamContext



```php
private static createStreamContext(array $injectFaults): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$injectFaults` | **array** |  |





***

### shouldFail



```php
private shouldFail(string $function): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$function` | **string** |  |





***


***
> Automatically generated on 2025-03-15
