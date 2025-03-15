
# QRCode

Turns a text string into a Model 2 QR Code



* Full name: `\chillerlan\QRCode\QRCode`

**See Also:**

* https://github.com/kazuhikoarase/qrcode-generator/tree/master/php - 
* http://www.qrcode.com/en/codes/model12.html - 
* https://www.swisseduc.ch/informatik/theoretische_informatik/qr_codes/docs/qr_standard.pdf - 
* https://en.wikipedia.org/wiki/QR_code - 
* http://www.thonky.com/qr-code-tutorial/ - 


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`VERSION_AUTO`|public|int|-1|
|`MASK_PATTERN_AUTO`|public|int|-1|
|`DATA_NUMBER`|public|int|0b1|
|`DATA_ALPHANUM`|public|int|0b10|
|`DATA_BYTE`|public|int|0b100|
|`DATA_KANJI`|public|int|0b1000|
|`DATA_MODES`|public|int[]|[self::DATA_NUMBER =&gt; 0, self::DATA_ALPHANUM =&gt; 1, self::DATA_BYTE =&gt; 2, self::DATA_KANJI =&gt; 3]|
|`ECC_L`|public|int|0b1|
|`ECC_M`|public|int|0b0|
|`ECC_Q`|public|int|0b11|
|`ECC_H`|public|int|0b10|
|`ECC_MODES`|public|int[]|[self::ECC_L =&gt; 0, self::ECC_M =&gt; 1, self::ECC_Q =&gt; 2, self::ECC_H =&gt; 3]|
|`OUTPUT_MARKUP_HTML`|public|string|&#039;html&#039;|
|`OUTPUT_MARKUP_SVG`|public|string|&#039;svg&#039;|
|`OUTPUT_IMAGE_PNG`|public|string|&#039;png&#039;|
|`OUTPUT_IMAGE_JPG`|public|string|&#039;jpg&#039;|
|`OUTPUT_IMAGE_GIF`|public|string|&#039;gif&#039;|
|`OUTPUT_STRING_JSON`|public|string|&#039;json&#039;|
|`OUTPUT_STRING_TEXT`|public|string|&#039;text&#039;|
|`OUTPUT_IMAGICK`|public|string|&#039;imagick&#039;|
|`OUTPUT_FPDF`|public|string|&#039;fpdf&#039;|
|`OUTPUT_CUSTOM`|public|string|&#039;custom&#039;|
|`OUTPUT_MODES`|public|string[][]|[\chillerlan\QRCode\Output\QRMarkup::class =&gt; [self::OUTPUT_MARKUP_SVG, self::OUTPUT_MARKUP_HTML], \chillerlan\QRCode\Output\QRImage::class =&gt; [self::OUTPUT_IMAGE_PNG, self::OUTPUT_IMAGE_GIF, self::OUTPUT_IMAGE_JPG], \chillerlan\QRCode\Output\QRString::class =&gt; [self::OUTPUT_STRING_JSON, self::OUTPUT_STRING_TEXT], \chillerlan\QRCode\Output\QRImagick::class =&gt; [self::OUTPUT_IMAGICK], \chillerlan\QRCode\Output\QRFpdf::class =&gt; [self::OUTPUT_FPDF]]|
|`DATA_INTERFACES`|protected|string[]|[&#039;number&#039; =&gt; \chillerlan\QRCode\Data\Number::class, &#039;alphanum&#039; =&gt; \chillerlan\QRCode\Data\AlphaNum::class, &#039;kanji&#039; =&gt; \chillerlan\QRCode\Data\Kanji::class, &#039;byte&#039; =&gt; \chillerlan\QRCode\Data\Byte::class]|

## Properties


### options

The settings container

```php
protected \chillerlan\QRCode\QROptions|\chillerlan\Settings\SettingsContainerInterface $options
```






***

### dataInterface

The selected data interface (Number, AlphaNum, Kanji, Byte)

```php
protected \chillerlan\QRCode\Data\QRDataInterface $dataInterface
```






***

## Methods


### __construct

QRCode constructor.

```php
public __construct(\chillerlan\Settings\SettingsContainerInterface $options = null): mixed
```

Sets the options instance, determines the current mb-encoding and sets it to UTF-8






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **\chillerlan\Settings\SettingsContainerInterface** |  |





***

### render

Renders a QR Code for the given $data and QROptions

```php
public render(string $data, string $file = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |
| `$file` | **string** |  |





***

### getMatrix

Returns a QRMatrix object for the given $data and current QROptions

```php
public getMatrix(string $data): \chillerlan\QRCode\Data\QRMatrix
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |




**Throws:**

- [`QRCodeDataException`](./Data/QRCodeDataException.md)



***

### initDataInterface

returns a fresh QRDataInterface for the given $data

```php
public initDataInterface(string $data): \chillerlan\QRCode\Data\QRDataInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |




**Throws:**

- [`QRCodeDataException`](./Data/QRCodeDataException.md)



***

### initOutputInterface

returns a fresh (built-in) QROutputInterface

```php
protected initOutputInterface(string $data): \chillerlan\QRCode\Output\QROutputInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |




**Throws:**

- [`QRCodeOutputException`](./Output/QRCodeOutputException.md)



***

### isNumber

checks if a string qualifies as numeric

```php
public isNumber(string $string): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |





***

### isAlphaNum

checks if a string qualifies as alphanumeric

```php
public isAlphaNum(string $string): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |





***

### checkString

checks is a given $string matches the characters of a given $charmap, returns false on the first invalid occurence.

```php
protected checkString(string $string, array $charmap): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$charmap` | **array** |  |





***

### isKanji

checks if a string qualifies as Kanji

```php
public isKanji(string $string): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |





***

### isByte

a dummy

```php
public isByte(string $data): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***


***
> Automatically generated on 2025-03-15
