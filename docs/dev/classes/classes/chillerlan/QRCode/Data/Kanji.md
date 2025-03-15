***

# Kanji

Kanji mode: double-byte characters from the Shift JIS character set

ISO/IEC 18004:2000 Section 8.3.5
ISO/IEC 18004:2000 Section 8.4.5

* Full name: `\chillerlan\QRCode\Data\Kanji`
* Parent class: [`\chillerlan\QRCode\Data\QRDataAbstract`](./QRDataAbstract.md)
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### datamode

the current data mode: Num, Alphanum, Kanji, Byte

```php
protected int $datamode
```






***

### lengthBits

mode length bits for the version breakpoints 1-9, 10-26 and 27-40

```php
protected array $lengthBits
```

ISO/IEC 18004:2000 Table 3 - Number of bits in Character Count Indicator




***

## Methods


### getLength

returns the byte count of the $data string

```php
protected getLength(string $data): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### write

writes the actual data string to the BitBuffer

```php
protected write(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |




**Throws:**
<p>on an illegal character occurence</p>

- [`QRCodeDataException`](./QRCodeDataException.md)



***


## Inherited methods


### __construct

QRDataInterface constructor.

```php
public __construct(\chillerlan\Settings\SettingsContainerInterface $options, string $data = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **\chillerlan\Settings\SettingsContainerInterface** |  |
| `$data` | **string** |  |





***

### setData

Sets the data string (internally called by the constructor)

```php
public setData(string $data): \chillerlan\QRCode\Data\QRDataInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### initMatrix

returns a fresh matrix object with the data written for the given $maskPattern

```php
public initMatrix(int $maskPattern, bool $test = null): \chillerlan\QRCode\Data\QRMatrix
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maskPattern` | **int** |  |
| `$test` | **bool** |  |





***

### getLengthBits

returns the length bits for the version breakpoints 1-9, 10-26 and 27-40

```php
protected getLengthBits(): int
```











**Throws:**

- [`QRCodeDataException`](./QRCodeDataException.md)



***

### getLength

returns the byte count of the $data string

```php
protected getLength(string $data): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### getMinimumVersion

returns the minimum version number for the given string

```php
protected getMinimumVersion(): int
```











**Throws:**

- [`QRCodeDataException`](./QRCodeDataException.md)



***

### write

writes the actual data string to the BitBuffer

```php
protected write(string $data): void
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





**See Also:**

* \chillerlan\QRCode\Data\QRDataAbstract::writeBitBuffer() - 

***

### writeBitBuffer

creates a BitBuffer and writes the string data to it

```php
protected writeBitBuffer(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |




**Throws:**
<p>on data overflow</p>

- [`QRCodeException`](../QRCodeException.md)



***

### maskECC

ECC masking

```php
protected maskECC(): array
```

ISO/IEC 18004:2000 Section 8.5 ff










**See Also:**

* http://www.thonky.com/qr-code-tutorial/error-correction-coding - 

***

### poly

helper method for the polynomial operations

```php
protected poly(int $key, int $count): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |
| `$count` | **int** |  |





***


***
> Automatically generated on 2025-03-15
