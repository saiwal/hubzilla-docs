***

# QRImage

Converts the matrix into GD images, raw or base64 output (requires ext-gd)



* Full name: `\chillerlan\QRCode\Output\QRImage`
* Parent class: [`\chillerlan\QRCode\Output\QROutputAbstract`](./QROutputAbstract.md)

**See Also:**

* http://php.net/manual/book.image.php - 


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TRANSPARENCY_TYPES`|protected|string[]|[\chillerlan\QRCode\QRCode::OUTPUT_IMAGE_PNG, \chillerlan\QRCode\QRCode::OUTPUT_IMAGE_GIF]|

## Properties


### defaultMode

the default output mode of the current output module

```php
protected string $defaultMode
```






***

### image

The GD image resource

```php
protected resource|\GdImage $image
```





**See Also:**

* \chillerlan\QRCode\Output\imagecreatetruecolor() - 

***

## Methods


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

- [`QRCodeException`](../QRCodeException.md)



***

### setModuleValues

Sets the initial module values (clean-up & defaults)

```php
protected setModuleValues(): void
```












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

- [`QRCodeOutputException`](./QRCodeOutputException.md)



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





***

### setModuleValues

Sets the initial module values (clean-up & defaults)

```php
protected setModuleValues(): void
```




* This method is **abstract**.







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

- [`QRCodeOutputException`](./QRCodeOutputException.md)



**See Also:**

* \chillerlan\QRCode\Output\file_put_contents() - * \chillerlan\QRCode\QROptions::cachefile - 

***

### dump

generates the output, optionally dumps it to a file, and returns it

```php
public dump(string $file = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***


***
> Automatically generated on 2025-03-15
