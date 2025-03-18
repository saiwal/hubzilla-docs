
# SessionRedis





* Full name: `\Zotlabs\Web\SessionRedis`
* This class implements:
[`\SessionHandlerInterface`](../../SessionHandlerInterface.md)



## Properties


### redis



```php
private $redis
```






***

## Methods


### __construct



```php
public __construct(mixed $connection): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$connection` | **mixed** |  |





***

### open



```php
public open(mixed $s, mixed $n): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |
| `$n` | **mixed** |  |





***

### read



```php
public read(mixed $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### write



```php
public write(mixed $id, mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |
| `$data` | **mixed** |  |





***

### close



```php
public close(): mixed
```












***

### destroy



```php
public destroy(mixed $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### gc



```php
public gc(mixed $expire): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$expire` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
