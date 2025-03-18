
# EndlessCycleStream





* Full name: `\ZipStream\Test\EndlessCycleStream`
* This class implements:
[`\Psr\Http\Message\StreamInterface`](../../Psr/Http/Message/StreamInterface.md)



## Properties


### offset



```php
private int $offset
```






***

### toRepeat



```php
private string $toRepeat
```






***

## Methods


### __construct



```php
public __construct(string $toRepeat = &#039;0&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$toRepeat` | **string** |  |





***

### __toString



```php
public __toString(): string
```












***

### close



```php
public close(): void
```












***

### detach



```php
public detach(): null
```












***

### getSize



```php
public getSize(): ?int
```












***

### tell



```php
public tell(): int
```












***

### eof



```php
public eof(): bool
```












***

### isSeekable



```php
public isSeekable(): bool
```












***

### seek



```php
public seek(int $offset, int $whence = SEEK_SET): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |
| `$whence` | **int** |  |





***

### rewind



```php
public rewind(): void
```












***

### isWritable



```php
public isWritable(): bool
```












***

### write



```php
public write(string $string): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |





***

### isReadable



```php
public isReadable(): bool
```












***

### read



```php
public read(int $length): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** |  |





***

### getContents



```php
public getContents(): string
```












***

### getMetadata



```php
public getMetadata(?string $key = null): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **?string** |  |





***


***
> Automatically generated on 2025-03-18
