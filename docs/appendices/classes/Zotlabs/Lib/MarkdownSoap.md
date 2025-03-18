
# MarkdownSoap





* Full name: `\Zotlabs\Lib\MarkdownSoap`



## Properties


### str



```php
private string $str
```






***

### token



```php
private string $token
```






***

## Methods


### __construct



```php
public __construct(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### clean



```php
public clean(): mixed
```












***

### extract_code



```php
public extract_code(string $s): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **string** |  |





**See Also:**

* \Zotlabs\Lib\encode_code() - * \Zotlabs\Lib\putback_code() - 

***

### encode_code



```php
public encode_code(mixed $matches): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **mixed** |  |





***

### decode_code



```php
public decode_code(mixed $matches): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **mixed** |  |





***

### putback_code



```php
public putback_code(string $s): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **string** |  |





**See Also:**

* \Zotlabs\Lib\extract_code() - * \Zotlabs\Lib\decode_code() - 

***

### purify



```php
public purify(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### protect_autolinks



```php
public protect_autolinks(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### unprotect_autolinks



```php
public unprotect_autolinks(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### escape



```php
public escape(mixed $s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### unescape



```php
public static unescape(string $s): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **string** |  |





***


***
> Automatically generated on 2025-03-18
