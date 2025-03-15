***

# HOTP





* Full name: `\OTPHP\HOTP`
* Parent class: [`\OTPHP\OTP`](./OTP.md)
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\OTPHP\HOTPInterface`](./HOTPInterface.md)
* This class is a **Final class**

**See Also:**

* \OTPHP\Test\HOTPTest - 


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DEFAULT_WINDOW`|private| |0|


## Methods


### create

Create a new HOTP object.

```php
public static create(null|string $secret = null, int $counter = self::DEFAULT_COUNTER, string $digest = self::DEFAULT_DIGEST, int $digits = self::DEFAULT_DIGITS): self
```

If the secret is null, a random 64 bytes secret will be generated.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$secret` | **null&#124;string** |  |
| `$counter` | **int** |  |
| `$digest` | **string** |  |
| `$digits` | **int** |  |





***

### createFromSecret

Create a OTP object from an existing secret.

```php
public static createFromSecret(string $secret): self
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$secret` | **string** |  |





***

### generate

Create a new OTP object. A random 64 bytes secret will be generated.

```php
public static generate(): self
```



* This method is **static**.








***

### getCounter

The initial counter (a positive integer).

```php
public getCounter(): 0|positive-int
```












***

### getProvisioningUri

Get the provisioning URI.

```php
public getProvisioningUri(): non-empty-string
```












***

### verify

If the counter is not provided, the OTP is verified at the actual counter.

```php
public verify(string $otp, null|int $counter = null, null|int $window = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$otp` | **string** |  |
| `$counter` | **null&#124;int** |  |
| `$window` | **null&#124;int** |  |





***

### setCounter



```php
public setCounter(int $counter): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$counter` | **int** |  |





***

### getParameterMap



```php
protected getParameterMap(): array&lt;non-empty-string,callable&gt;
```












***

### updateCounter



```php
private updateCounter(positive-int $counter): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$counter` | **positive-int** |  |





***

### getWindow



```php
private getWindow(null|0|positive-int $window): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$window` | **null&#124;0&#124;positive-int** |  |





***

### verifyOtpWithWindow



```php
private verifyOtpWithWindow(non-empty-string $otp, 0|positive-int $counter, null|0|positive-int $window): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$otp` | **non-empty-string** |  |
| `$counter` | **0&#124;positive-int** |  |
| `$window` | **null&#124;0&#124;positive-int** |  |





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


***
> Automatically generated on 2025-03-15
