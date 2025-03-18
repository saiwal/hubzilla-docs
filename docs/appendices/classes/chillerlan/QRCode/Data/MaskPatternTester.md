
# MaskPatternTester

Receives a QRDataInterface object and runs the mask pattern tests on it.

ISO/IEC 18004:2000 Section 8.8.2 - Evaluation of masking results

* Full name: `\chillerlan\QRCode\Data\MaskPatternTester`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**

**See Also:**

* http://www.thonky.com/qr-code-tutorial/data-masking - 



## Properties


### dataInterface

The data interface that contains the data matrix to test

```php
protected \chillerlan\QRCode\Data\QRDataInterface $dataInterface
```






***

## Methods


### __construct

Receives the QRDataInterface

```php
public __construct(\chillerlan\QRCode\Data\QRDataInterface $dataInterface): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dataInterface` | **\chillerlan\QRCode\Data\QRDataInterface** |  |





**See Also:**

* \chillerlan\QRCode\QROptions::$maskPattern - * \chillerlan\QRCode\Data\QRMatrix::$maskPattern - 

***

### getBestMaskPattern

shoves a QRMatrix through the MaskPatternTester to find the lowest penalty mask pattern

```php
public getBestMaskPattern(): int
```












**See Also:**

* \chillerlan\QRCode\Data\MaskPatternTester - 

***

### testPattern

Returns the penalty for the given mask pattern

```php
public testPattern(int $pattern): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pattern` | **int** |  |





**See Also:**

* \chillerlan\QRCode\QROptions::$maskPattern - * \chillerlan\QRCode\Data\QRMatrix::$maskPattern - 

***

### testLevel1

Checks for each group of five or more same-colored modules in a row (or column)

```php
protected testLevel1(array $m, int $size): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **array** |  |
| `$size` | **int** |  |





***

### testLevel2

Checks for each 2x2 area of same-colored modules in the matrix

```php
protected testLevel2(array $m, int $size): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **array** |  |
| `$size` | **int** |  |





***

### testLevel3

Checks if there are patterns that look similar to the finder patterns (1:1:3:1:1 ratio)

```php
protected testLevel3(array $m, int $size): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **array** |  |
| `$size` | **int** |  |





***

### testLevel4

Checks if more than half of the modules are dark or light, with a larger penalty for a larger difference

```php
protected testLevel4(array $m, int $size): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **array** |  |
| `$size` | **int** |  |





***


***
> Automatically generated on 2025-03-18
