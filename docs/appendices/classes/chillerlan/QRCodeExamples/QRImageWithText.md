
# QRImageWithText

Converts the matrix into GD images, raw or base64 output (requires ext-gd)



* Full name: `\chillerlan\QRCodeExamples\QRImageWithText`
* Parent class: [`\chillerlan\QRCode\Output\QRImage`](../QRCode/Output/QRImage.md)




## Methods


### dump

generates the output, optionally dumps it to a file, and returns it

```php
public dump(string|null $file = null, string|null $text = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string&#124;null** |  |
| `$text` | **string&#124;null** |  |





***

### addText



```php
protected addText(string $text): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***


## Inherited methods


### __construct

QROutputAbstract constructor.

```php
public __construct(\chillerlan\Settings\SettingsContainerInterface $options, \chillerlan\QRCode\Data\QRMatrix $matrix): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **\chillerlan\Settings\SettingsContainerInterface** |  |
| `$matrix` | **\chillerlan\QRCode\Data\QRMatrix** |  |




**Throws:**

- [`QRCodeException`](../QRCode/QRCodeException.md)



***

### setModuleValues

Sets the initial module values (clean-up & defaults)

```php
protected setModuleValues(): void
```












***

### saveToFile

saves the qr data to a file

```php
protected saveToFile(string $data, string $file): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |
| `$file` | **string** |  |




**Throws:**

- [`QRCodeOutputException`](../QRCode/Output/QRCodeOutputException.md)



**See Also:**

* \chillerlan\QRCode\Output\file_put_contents() - * \chillerlan\QRCode\QROptions::cachefile - 

***

### dump

generates the output, optionally dumps it to a file, and returns it

```php
public dump(string $file = null): string|resource|\GdImage
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***

### setPixel

Creates a single QR pixel with the given settings

```php
protected setPixel(int $x, int $y, array $rgb): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** |  |
| `$y` | **int** |  |
| `$rgb` | **array** |  |





***

### dumpImage

Creates the final image by calling the desired GD output function

```php
protected dumpImage(): string
```











**Throws:**

- [`QRCodeOutputException`](../QRCode/Output/QRCodeOutputException.md)



***

### png

PNG output

```php
protected png(): void
```












***

### gif

Jiff - like... JitHub!

```php
protected gif(): void
```












***

### jpg

JPG output

```php
protected jpg(): void
```












***


***
> Automatically generated on 2025-03-18
