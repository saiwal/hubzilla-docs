***

# QRMatrix

Holds a numerical representation of the final QR Code;
maps the ECC coded binary data and applies the mask pattern



* Full name: `\chillerlan\QRCode\Data\QRMatrix`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**

**See Also:**

* http://www.thonky.com/qr-code-tutorial/format-version-information - 


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`M_NULL`|public|int|0x0|
|`M_DARKMODULE`|public|int|0x2|
|`M_DATA`|public|int|0x4|
|`M_FINDER`|public|int|0x6|
|`M_SEPARATOR`|public|int|0x8|
|`M_ALIGNMENT`|public|int|0xa|
|`M_TIMING`|public|int|0xc|
|`M_FORMAT`|public|int|0xe|
|`M_VERSION`|public|int|0x10|
|`M_QUIETZONE`|public|int|0x12|
|`M_LOGO`|public|int|0x14|
|`M_FINDER_DOT`|public|int|0x16|
|`M_TEST`|public|int|0xff|
|`alignmentPattern`|protected|int[][]|[1 =&gt; [], 2 =&gt; [6, 18], 3 =&gt; [6, 22], 4 =&gt; [6, 26], 5 =&gt; [6, 30], 6 =&gt; [6, 34], 7 =&gt; [6, 22, 38], 8 =&gt; [6, 24, 42], 9 =&gt; [6, 26, 46], 10 =&gt; [6, 28, 50], 11 =&gt; [6, 30, 54], 12 =&gt; [6, 32, 58], 13 =&gt; [6, 34, 62], 14 =&gt; [6, 26, 46, 66], 15 =&gt; [6, 26, 48, 70], 16 =&gt; [6, 26, 50, 74], 17 =&gt; [6, 30, 54, 78], 18 =&gt; [6, 30, 56, 82], 19 =&gt; [6, 30, 58, 86], 20 =&gt; [6, 34, 62, 90], 21 =&gt; [6, 28, 50, 72, 94], 22 =&gt; [6, 26, 50, 74, 98], 23 =&gt; [6, 30, 54, 78, 102], 24 =&gt; [6, 28, 54, 80, 106], 25 =&gt; [6, 32, 58, 84, 110], 26 =&gt; [6, 30, 58, 86, 114], 27 =&gt; [6, 34, 62, 90, 118], 28 =&gt; [6, 26, 50, 74, 98, 122], 29 =&gt; [6, 30, 54, 78, 102, 126], 30 =&gt; [6, 26, 52, 78, 104, 130], 31 =&gt; [6, 30, 56, 82, 108, 134], 32 =&gt; [6, 34, 60, 86, 112, 138], 33 =&gt; [6, 30, 58, 86, 114, 142], 34 =&gt; [6, 34, 62, 90, 118, 146], 35 =&gt; [6, 30, 54, 78, 102, 126, 150], 36 =&gt; [6, 24, 50, 76, 102, 128, 154], 37 =&gt; [6, 28, 54, 80, 106, 132, 158], 38 =&gt; [6, 32, 58, 84, 110, 136, 162], 39 =&gt; [6, 26, 54, 82, 110, 138, 166], 40 =&gt; [6, 30, 58, 86, 114, 142, 170]]|
|`versionPattern`|protected|int[]|[7 =&gt; 0b111110010010100, 8 =&gt; 0b1000010110111100, 9 =&gt; 0b1001101010011001, 10 =&gt; 0b1010010011010011, 11 =&gt; 0b1011101111110110, 12 =&gt; 0b1100011101100010, 13 =&gt; 0b1101100001000111, 14 =&gt; 0b1110011000001101, 15 =&gt; 0b1111100100101000, 16 =&gt; 0b10000101101111000, 17 =&gt; 0b10001010001011101, 18 =&gt; 0b10010101000010111, 19 =&gt; 0b10011010100110010, 20 =&gt; 0b10100100110100110, 21 =&gt; 0b10101011010000011, 22 =&gt; 0b10110100011001001, 23 =&gt; 0b10111011111101100, 24 =&gt; 0b11000111011000100, 25 =&gt; 0b11001000111100001, 26 =&gt; 0b11010111110101011, 27 =&gt; 0b11011000010001110, 28 =&gt; 0b11100110000011010, 29 =&gt; 0b11101001100111111, 30 =&gt; 0b11110110101110101, 31 =&gt; 0b11111001001010000, 32 =&gt; 0b100000100111010101, 33 =&gt; 0b100001011011110000, 34 =&gt; 0b100010100010111010, 35 =&gt; 0b100011011110011111, 36 =&gt; 0b100100101100001011, 37 =&gt; 0b100101010000101110, 38 =&gt; 0b100110101001100100, 39 =&gt; 0b100111010101000001, 40 =&gt; 0b101000110001101001]|
|`formatPattern`|protected|int[][]|[[
    // L
    0b111011111000100,
    0b111001011110011,
    0b111110110101010,
    0b111100010011101,
    0b110011000101111,
    0b110001100011000,
    0b110110001000001,
    0b110100101110110,
], [
    // M
    0b101010000010010,
    0b101000100100101,
    0b101111001111100,
    0b101101101001011,
    0b100010111111001,
    0b100000011001110,
    0b100111110010111,
    0b100101010100000,
], [
    // Q
    0b11010101011111,
    0b11000001101000,
    0b11111100110001,
    0b11101000000110,
    0b10010010110100,
    0b10000110000011,
    0b10111011011010,
    0b10101111101101,
], [
    // H
    0b1011010001001,
    0b1001110111110,
    0b1110011100111,
    0b1100111010000,
    0b11101100010,
    0b1001010101,
    0b110100001100,
    0b100000111011,
]]|

## Properties


### version

the current QR Code version number

```php
protected int $version
```






***

### eclevel

the current ECC level

```php
protected int $eclevel
```






***

### maskPattern

the used mask pattern, set via QRMatrix::mapData()

```php
protected int $maskPattern
```






***

### moduleCount

the size (side length) of the matrix

```php
protected int $moduleCount
```






***

### matrix

the actual matrix data array

```php
protected int[][] $matrix
```






***

## Methods


### __construct

QRMatrix constructor.

```php
public __construct(int $version, int $eclevel): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |
| `$eclevel` | **int** |  |




**Throws:**

- [`QRCodeDataException`](./QRCodeDataException.md)



***

### init

shortcut to initialize the matrix

```php
public init(int $maskPattern, bool $test = null): \chillerlan\QRCode\Data\QRMatrix
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maskPattern` | **int** |  |
| `$test` | **bool** |  |





***

### matrix

Returns the data matrix, returns a pure boolean representation if $boolean is set to true

```php
public matrix(bool $boolean = false): int[][]|bool[][]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$boolean` | **bool** |  |





***

### version

Returns the current version number

```php
public version(): int
```












***

### eccLevel

Returns the current ECC level

```php
public eccLevel(): int
```












***

### maskPattern

Returns the current mask pattern

```php
public maskPattern(): int
```












***

### size

Returns the absoulute size of the matrix, including quiet zone (after setting it).

```php
public size(): int
```

size = version * 4 + 17 [ + 2 * quietzone size]










***

### get

Returns the value of the module at position [$x, $y]

```php
public get(int $x, int $y): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** |  |
| `$y` | **int** |  |





***

### set

Sets the $M_TYPE value for the module at position [$x, $y]

```php
public set(int $x, int $y, bool $value, int $M_TYPE): \chillerlan\QRCode\Data\QRMatrix
```

true  => $M_TYPE << 8
false => $M_TYPE






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** |  |
| `$y` | **int** |  |
| `$value` | **bool** |  |
| `$M_TYPE` | **int** |  |





***

### check

Checks whether a module is true (dark) or false (light)

```php
public check(int $x, int $y): bool
```

true  => $value >> 8 === $M_TYPE
         $value >> 8 > 0

false => $value === $M_TYPE
         $value >> 8 === 0






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** |  |
| `$y` | **int** |  |





***

### setDarkModule

Sets the "dark module", that is always on the same position 1x1px away from the bottom left finder

```php
public setDarkModule(): \chillerlan\QRCode\Data\QRMatrix
```












***

### setFinderPattern

Draws the 7x7 finder patterns in the corners top left/right and bottom left

```php
public setFinderPattern(): \chillerlan\QRCode\Data\QRMatrix
```

ISO/IEC 18004:2000 Section 7.3.2










***

### setSeparators

Draws the separator lines around the finder patterns

```php
public setSeparators(): \chillerlan\QRCode\Data\QRMatrix
```

ISO/IEC 18004:2000 Section 7.3.3










***

### setAlignmentPattern

Draws the 5x5 alignment patterns

```php
public setAlignmentPattern(): \chillerlan\QRCode\Data\QRMatrix
```

ISO/IEC 18004:2000 Section 7.3.5










***

### setTimingPattern

Draws the timing pattern (h/v checkered line between the finder patterns)

```php
public setTimingPattern(): \chillerlan\QRCode\Data\QRMatrix
```

ISO/IEC 18004:2000 Section 7.3.4










***

### setVersionNumber

Draws the version information, 2x 3x6 pixel

```php
public setVersionNumber(bool $test = null): \chillerlan\QRCode\Data\QRMatrix
```

ISO/IEC 18004:2000 Section 8.10






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **bool** |  |





***

### setFormatInfo

Draws the format info along the finder patterns

```php
public setFormatInfo(int $maskPattern, bool $test = null): \chillerlan\QRCode\Data\QRMatrix
```

ISO/IEC 18004:2000 Section 8.9






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maskPattern` | **int** |  |
| `$test` | **bool** |  |





***

### setQuietZone

Draws the "quiet zone" of $size around the matrix

```php
public setQuietZone(int $size = null): \chillerlan\QRCode\Data\QRMatrix
```

ISO/IEC 18004:2000 Section 7.3.7






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$size` | **int** |  |




**Throws:**

- [`QRCodeDataException`](./QRCodeDataException.md)



***

### setLogoSpace

Clears a space of $width * $height in order to add a logo or text.

```php
public setLogoSpace(int $width, int $height, int $startX = null, int $startY = null): \chillerlan\QRCode\Data\QRMatrix
```

Additionally, the logo space can be positioned within the QR Code - respecting the main functional patterns -
using $startX and $startY. If either of these are null, the logo space will be centered in that direction.
ECC level "H" (30%) is required.

Please note that adding a logo space minimizes the error correction capacity of the QR Code and
created images may become unreadable, especially when printed with a chance to receive damage.
Please test thoroughly before using this feature in production.

This method should be called from within an output module (after the matrix has been filled with data).
Note that there is no restiction on how many times this method could be called on the same matrix instance.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** |  |
| `$height` | **int** |  |
| `$startX` | **int** |  |
| `$startY` | **int** |  |




**Throws:**

- [`QRCodeDataException`](./QRCodeDataException.md)



**See Also:**

* https://github.com/chillerlan/php-qrcode/issues/52 - 

***

### mapData

Maps the binary $data array from QRDataInterface::maskECC() on the matrix,
masking the data using $maskPattern (ISO/IEC 18004:2000 Section 8.8)

```php
public mapData(int[] $data, int $maskPattern): \chillerlan\QRCode\Data\QRMatrix
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **int[]** |  |
| `$maskPattern` | **int** |  |





**See Also:**

* \chillerlan\QRCode\Data\QRDataAbstract::maskECC() - 

***


***
> Automatically generated on 2025-03-15
