
# OTP





* Full name: `\OTPHP\OTP`
* This class implements:
[`\OTPHP\OTPInterface`](./OTPInterface.md)
* This class is an **Abstract class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DEFAULT_SECRET_SIZE`|private| |64|


## Methods


### __construct



```php
protected __construct(non-empty-string $secret): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$secret` | **non-empty-string** |  |





***

### getQrCodeUri

Get the provisioning URI.

```php
public getQrCodeUri(string $uri, string $placeholder): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** | The Uri of the QRCode generator with all parameters. This Uri MUST contain a placeholder that will be replaced by the method. |
| `$placeholder` | **string** | the placeholder to be replaced in the QR Code generator URI |





***

### at



```php
public at(int $input): non-empty-string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **int** |  |


**Return Value:**

Return the OTP at the specified timestamp




***

### generateSecret



```php
final protected static generateSecret(): non-empty-string
```



* This method is **static**.

* This method is **final**.






***

### generateOTP

The OTP at the specified input.

```php
protected generateOTP(0|positive-int $input): non-empty-string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **0&#124;positive-int** |  |





***

### filterOptions



```php
protected filterOptions(array&lt;non-empty-string,mixed&gt;& $options): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **array<non-empty-string,mixed>** |  |





***

### generateURI



```php
protected generateURI(non-empty-string $type, array&lt;non-empty-string,mixed&gt; $options): non-empty-string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **non-empty-string** |  |
| `$options` | **array<non-empty-string,mixed>** |  |





***

### compareOTP



```php
protected compareOTP(non-empty-string $safe, non-empty-string $user): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$safe` | **non-empty-string** |  |
| `$user` | **non-empty-string** |  |





***

### getDecodedSecret



```php
private getDecodedSecret(): non-empty-string
```












***

### intToByteString



```php
private intToByteString(0|positive-int $int): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$int` | **0&#124;positive-int** |  |





***


## Inherited methods


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
