***

# Keyutils

Keyutils
Convert RSA keys between various formats



* Full name: `\Zotlabs\Lib\Keyutils`




## Methods


### meToPem



```php
public static meToPem(string $m, string $e): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **string** | modulo |
| `$e` | **string** | exponent |





***

### rsaToPem



```php
public static rsaToPem(mixed $key): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### pemToRsa



```php
public static pemToRsa(mixed $key): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### pemToMe



```php
public static pemToMe(string $key, string& $m, string& $e): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | key |
| `$m` | **string** | reference modulo |
| `$e` | **string** | reference exponent |





***

### salmonKey



```php
public static salmonKey(string $pubkey): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pubkey` | **string** |  |





***

### convertSalmonKey



```php
public static convertSalmonKey(string $key): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |





***


***
> Automatically generated on 2025-03-15
