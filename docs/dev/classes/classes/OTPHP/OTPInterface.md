***

# OTPInterface





* Full name: `\OTPHP\OTPInterface`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DEFAULT_DIGITS`|public| |6|
|`DEFAULT_DIGEST`|public| |&#039;sha1&#039;|

## Methods


### createFromSecret

Create a OTP object from an existing secret.

```php
public static createFromSecret(non-empty-string $secret): self
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$secret` | **non-empty-string** |  |





***

### generate

Create a new OTP object. A random 64 bytes secret will be generated.

```php
public static generate(): self
```



* This method is **static**.








***

### setSecret



```php
public setSecret(non-empty-string $secret): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$secret` | **non-empty-string** |  |





***

### setDigits



```php
public setDigits(positive-int $digits): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$digits` | **positive-int** |  |





***

### setDigest



```php
public setDigest(non-empty-string $digest): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$digest` | **non-empty-string** |  |





***

### at



```php
public at(0|positive-int $input): non-empty-string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **0&#124;positive-int** |  |


**Return Value:**

Return the OTP at the specified timestamp




***

### verify

Verify that the OTP is valid with the specified input. If no input is provided, the input is set to a default
value or false is returned.

```php
public verify(non-empty-string $otp, null|0|positive-int $input = null, null|0|positive-int $window = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$otp` | **non-empty-string** |  |
| `$input` | **null&#124;0&#124;positive-int** |  |
| `$window` | **null&#124;0&#124;positive-int** |  |





***

### getSecret



```php
public getSecret(): non-empty-string
```









**Return Value:**

The secret of the OTP




***

### setLabel



```php
public setLabel(non-empty-string $label): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$label` | **non-empty-string** | The label of the OTP |





***

### getLabel



```php
public getLabel(): non-empty-string|null
```









**Return Value:**

The label of the OTP




***

### getIssuer



```php
public getIssuer(): non-empty-string|null
```









**Return Value:**

The issuer




***

### setIssuer



```php
public setIssuer(non-empty-string $issuer): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$issuer` | **non-empty-string** |  |





***

### isIssuerIncludedAsParameter



```php
public isIssuerIncludedAsParameter(): bool
```









**Return Value:**

If true, the issuer will be added as a parameter in the provisioning URI




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
public getDigits(): positive-int
```









**Return Value:**

Number of digits in the OTP




***

### getDigest



```php
public getDigest(): non-empty-string
```









**Return Value:**

Digest algorithm used to calculate the OTP. Possible values are 'md5', 'sha1', 'sha256' and 'sha512'




***

### getParameter



```php
public getParameter(non-empty-string $parameter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameter` | **non-empty-string** |  |





***

### hasParameter



```php
public hasParameter(non-empty-string $parameter): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameter` | **non-empty-string** |  |





***

### getParameters



```php
public getParameters(): array&lt;non-empty-string,mixed&gt;
```












***

### setParameter



```php
public setParameter(non-empty-string $parameter, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parameter` | **non-empty-string** |  |
| `$value` | **mixed** |  |





***

### getProvisioningUri

Get the provisioning URI.

```php
public getProvisioningUri(): non-empty-string
```












***

### getQrCodeUri

Get the provisioning URI.

```php
public getQrCodeUri(non-empty-string $uri, non-empty-string $placeholder): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **non-empty-string** | The Uri of the QRCode generator with all parameters. This Uri MUST contain a placeholder that will be replaced by the method. |
| `$placeholder` | **non-empty-string** | the placeholder to be replaced in the QR Code generator URI |





***


***
> Automatically generated on 2025-03-15
