
# SessionHandler





* Full name: `\Zotlabs\Web\SessionHandler`
* This class implements:
[`\SessionHandlerInterface`](../../SessionHandlerInterface.md)




## Methods


### open



```php
public open(mixed $s, mixed $n): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |
| `$n` | **mixed** |  |





***

### read



```php
public read(mixed $id): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### write



```php
public write(mixed $id, mixed $data): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |
| `$data` | **mixed** |  |





***

### close



```php
public close(): bool
```












***

### destroy



```php
public destroy(mixed $id): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### gc



```php
public gc(mixed $expire): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$expire` | **mixed** |  |





***


***
> Automatically generated on 2025-03-19
