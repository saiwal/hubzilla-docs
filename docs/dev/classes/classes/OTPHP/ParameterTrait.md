***

# ParameterTrait





* Full name: `\OTPHP\ParameterTrait`



## Properties


### parameters



```php
private array&lt;non-empty-string,mixed&gt; $parameters
```






***

### issuer



```php
private non-empty-string|null $issuer
```






***

### label



```php
private non-empty-string|null $label
```






***

### issuer_included_as_parameter



```php
private bool $issuer_included_as_parameter
```






***

## Methods


### getParameters



```php
public getParameters(): array&lt;non-empty-string,mixed&gt;
```












***

### getSecret



```php
public getSecret(): string
```












***

### getLabel



```php
public getLabel(): null|string
```












***

### setLabel



```php
public setLabel(string $label): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$label` | **string** |  |





***

### getIssuer



```php
public getIssuer(): null|string
```












***

### setIssuer



```php
public setIssuer(string $issuer): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$issuer` | **string** |  |





***

### isIssuerIncludedAsParameter



```php
public isIssuerIncludedAsParameter(): bool
```












***

### setIssuerIncludedAsParameter



```php
public setIssuerIncludedAsParameter(bool $issuer_included_as_parameter): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$issuer_included_as_parameter` | **bool** |  |





***

### getDigits



```php
public getDigits(): int
```












***

### getDigest



```php
public getDigest(): string
```












***

### hasParameter



```php
public hasParameter(string $parameter): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameter` | **string** |  |





***

### getParameter



```php
public getParameter(string $parameter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameter` | **string** |  |





***

### setParameter



```php
public setParameter(string $parameter, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameter` | **string** |  |
| `$value` | **mixed** |  |





***

### setSecret



```php
public setSecret(string $secret): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$secret` | **string** |  |





***

### setDigits



```php
public setDigits(int $digits): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$digits` | **int** |  |





***

### setDigest



```php
public setDigest(string $digest): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$digest` | **string** |  |





***

### getParameterMap



```php
protected getParameterMap(): array&lt;non-empty-string,callable&gt;
```












***

### hasColon



```php
private hasColon(non-empty-string $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **non-empty-string** |  |





***

***
> Automatically generated on 2025-03-15

