***

# Configuration





* Full name: `\League\HTMLToMarkdown\Configuration`



## Properties


### config



```php
protected array&lt;string,mixed&gt; $config
```






***

## Methods


### __construct



```php
public __construct(array&lt;string,mixed&gt; $config = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **array<string,mixed>** |  |





***

### merge



```php
public merge(array&lt;string,mixed&gt; $config = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **array<string,mixed>** |  |





***

### replace



```php
public replace(array&lt;string,mixed&gt; $config = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **array<string,mixed>** |  |





***

### setOption



```php
public setOption(string $key, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$value` | **mixed** |  |





***

### getOption



```php
public getOption(?string $key = null, mixed|null $default = null): mixed|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **?string** |  |
| `$default` | **mixed&#124;null** |  |





***

### checkForDeprecatedOptions



```php
private checkForDeprecatedOptions(array&lt;string,mixed&gt; $config): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **array<string,mixed>** |  |





***


***
> Automatically generated on 2025-03-15
