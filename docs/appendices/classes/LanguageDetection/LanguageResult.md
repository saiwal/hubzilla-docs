
# LanguageResult

Class LanguageResult



* Full name: `\LanguageDetection\LanguageResult`
* This class implements:
[`\JsonSerializable`](../JsonSerializable.md), [`\IteratorAggregate`](../IteratorAggregate.md), [`\ArrayAccess`](../ArrayAccess.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`THRESHOLD`|public| |0.025|

## Properties


### result



```php
private array $result
```






***

## Methods


### __construct

LanguageResult constructor.

```php
public __construct(array $result = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$result` | **array** |  |





***

### offsetExists



```php
public offsetExists(mixed $offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |





***

### offsetGet



```php
public offsetGet(mixed $offset): mixed|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |





***

### offsetSet



```php
public offsetSet(mixed $offset, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |
| `$value` | **mixed** |  |





***

### offsetUnset



```php
public offsetUnset(mixed $offset): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |





***

### jsonSerialize



```php
public jsonSerialize(): array
```












***

### __toString



```php
public __toString(): string
```












***

### whitelist



```php
public whitelist(\string[] $whitelist): \LanguageDetection\LanguageResult
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$whitelist` | **\string[]** |  |





***

### blacklist



```php
public blacklist(\string[] $blacklist): \LanguageDetection\LanguageResult
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$blacklist` | **\string[]** |  |





***

### close



```php
public close(): array
```












***

### bestResults



```php
public bestResults(): \LanguageDetection\LanguageResult
```












***

### getIterator



```php
public getIterator(): \ArrayIterator
```












***

### limit



```php
public limit(int $offset, int|null $length = null): \LanguageDetection\LanguageResult
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |
| `$length` | **int&#124;null** |  |





***


***
> Automatically generated on 2025-03-18
