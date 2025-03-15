***

# QROutputAbstract

common output abstract



* Full name: `\chillerlan\QRCode\Output\QROutputAbstract`
* This class implements:
[`\chillerlan\QRCode\Output\QROutputInterface`](./QROutputInterface.md)
* This class is an **Abstract class**



## Properties


### moduleCount

the current size of the QR matrix

```php
protected int $moduleCount
```





**See Also:**

* \chillerlan\QRCode\Data\QRMatrix::size() - 

***

### outputMode

the current output mode

```php
protected string $outputMode
```





**See Also:**

* \chillerlan\QRCode\QROptions::$outputType - 

***

### defaultMode

the default output mode of the current output module

```php
protected string $defaultMode
```






***

### scale

the current scaling for a QR pixel

```php
protected int $scale
```





**See Also:**

* \chillerlan\QRCode\QROptions::$scale - 

***

### length

the side length of the QR image (modules * scale)

```php
protected int $length
```






***

### moduleValues

an (optional) array of color values for the several QR matrix parts

```php
protected array $moduleValues
```






***

### matrix

the (filled) data matrix object

```php
protected \chillerlan\QRCode\Data\QRMatrix $matrix
```






***

### options



```php
protected \chillerlan\Settings\SettingsContainerInterface|\chillerlan\QRCode\QROptions $options
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
