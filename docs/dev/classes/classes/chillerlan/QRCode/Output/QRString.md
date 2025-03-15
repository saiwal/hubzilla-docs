
# QRString

Converts the matrix data into string types



* Full name: `\chillerlan\QRCode\Output\QRString`
* Parent class: [`\chillerlan\QRCode\Output\QROutputAbstract`](./QROutputAbstract.md)



## Properties


### defaultMode

the default output mode of the current output module

```php
protected string $defaultMode
```






***

## Methods


### setModuleValues

Sets the initial module values (clean-up & defaults)

```php
protected setModuleValues(): void
```












***

### text

string output

```php
protected text(string $file = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***

### json

JSON output

```php
protected json(string $file = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





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
