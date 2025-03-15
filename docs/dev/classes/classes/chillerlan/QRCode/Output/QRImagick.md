
# QRImagick

ImageMagick output module (requires ext-imagick)



* Full name: `\chillerlan\QRCode\Output\QRImagick`
* Parent class: [`\chillerlan\QRCode\Output\QROutputAbstract`](./QROutputAbstract.md)

**See Also:**

* http://php.net/manual/book.imagick.php - 
* http://phpimagick.com - 



## Properties


### imagick



```php
protected \Imagick $imagick
```






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
public dump(string $file = null): string|\Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***

### drawImage

Creates the QR image via ImagickDraw

```php
protected drawImage(): void
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
