***

# QROptionsTrait

The QRCode plug-in settings & setter functionality



* Full name: `\chillerlan\QRCode\QROptionsTrait`



## Properties


### version

QR Code version number

```php
protected int $version
```

[1 ... 40] or QRCode::VERSION_AUTO




***

### versionMin

Minimum QR version

```php
protected int $versionMin
```

if $version = QRCode::VERSION_AUTO




***

### versionMax

Maximum QR version

```php
protected int $versionMax
```






***

### eccLevel

Error correct level

```php
protected int $eccLevel
```

QRCode::ECC_X where X is:

- L =>  7%
- M => 15%
- Q => 25%
- H => 30%




***

### maskPattern

Mask Pattern to use

```php
protected int $maskPattern
```

[0...7] or QRCode::MASK_PATTERN_AUTO




***

### addQuietzone

Add a "quiet zone" (margin) according to the QR code spec

```php
protected bool $addQuietzone
```






***

### quietzoneSize

Size of the quiet zone

```php
protected int $quietzoneSize
```

internally clamped to [0 ... $moduleCount / 2], defaults to 4 modules




***

### dataModeOverride

Use this to circumvent the data mode detection and force the usage of the given mode.

```php
protected string $dataModeOverride
```

valid modes are: Number, AlphaNum, Kanji, Byte (case insensitive)



**See Also:**

* https://github.com/chillerlan/php-qrcode/issues/39 - * https://github.com/chillerlan/php-qrcode/issues/97 - (changed default value to '')

***

### outputType

The output type

```php
protected string $outputType
```

- QRCode::OUTPUT_MARKUP_XXXX where XXXX = HTML, SVG
- QRCode::OUTPUT_IMAGE_XXX where XXX = PNG, GIF, JPG
- QRCode::OUTPUT_STRING_XXXX where XXXX = TEXT, JSON
- QRCode::OUTPUT_CUSTOM




***

### outputInterface

the FQCN of the custom QROutputInterface if $outputType is set to QRCode::OUTPUT_CUSTOM

```php
protected ?string $outputInterface
```






***

### cachefile

/path/to/cache.file

```php
protected ?string $cachefile
```






***

### eol

newline string [HTML, SVG, TEXT]

```php
protected string $eol
```






***

### scale

size of a QR code pixel [SVG, IMAGE_*], HTML via CSS

```php
protected int $scale
```






***

### cssClass

a common css class

```php
protected string $cssClass
```






***

### svgOpacity

SVG opacity

```php
protected float $svgOpacity
```






***

### svgDefs

anything between <defs>

```php
protected string $svgDefs
```





**See Also:**

* https://developer.mozilla.org/docs/Web/SVG/Element/defs - 

***

### svgViewBoxSize

SVG viewBox size. a single integer number which defines width/height of the viewBox attribute.

```php
protected ?int $svgViewBoxSize
```

viewBox="0 0 x x"



**See Also:**

* https://css-tricks.com/scale-svg/#article-header-id-3 - 

***

### textDark

string substitute for dark

```php
protected string $textDark
```






***

### textLight

string substitute for light

```php
protected string $textLight
```






***

### markupDark

markup substitute for dark (CSS value)

```php
protected string $markupDark
```






***

### markupLight

markup substitute for light (CSS value)

```php
protected string $markupLight
```






***

### returnResource

Return the image resource instead of a render if applicable.

```php
protected bool $returnResource
```

This option overrides other output options, such as $cachefile and $imageBase64.

Supported by the following modules:

- QRImage:   resource (PHP < 8), GdImage
- QRImagick: Imagick
- QRFpdf:    FPDF



**See Also:**

* \chillerlan\QRCode\Output\QROutputInterface::dump() - 

***

### imageBase64

toggle base64 or raw image data

```php
protected bool $imageBase64
```






***

### imageTransparent

toggle transparency, not supported by jpg

```php
protected bool $imageTransparent
```






***

### imageTransparencyBG



```php
protected array $imageTransparencyBG
```





**See Also:**

* \chillerlan\QRCode\imagecolortransparent() - [R, G, B]

***

### pngCompression



```php
protected int $pngCompression
```





**See Also:**

* \chillerlan\QRCode\imagepng() - 

***

### jpegQuality



```php
protected int $jpegQuality
```





**See Also:**

* \chillerlan\QRCode\imagejpeg() - 

***

### imagickFormat

Imagick output format

```php
protected string $imagickFormat
```





**See Also:**

* \Imagick::setType() - 

***

### imagickBG

Imagick background color (defaults to "transparent")

```php
protected ?string $imagickBG
```





**See Also:**

* \ImagickPixel::__construct() - 

***

### fpdfMeasureUnit

Measurement unit for FPDF output: pt, mm, cm, in (defaults to "pt")

```php
protected string $fpdfMeasureUnit
```





**See Also:**

* \FPDF::__construct() - 

***

### moduleValues

Module values map

```php
protected ?array $moduleValues
```

- HTML, IMAGICK: #ABCDEF, cssname, rgb(), rgba()...
- IMAGE: [63, 127, 255] // R, G, B




***

## Methods


### setMinMaxVersion

clamp min/max version number

```php
protected setMinMaxVersion(int $versionMin, int $versionMax): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$versionMin` | **int** |  |
| `$versionMax` | **int** |  |





***

### set_versionMin

sets the minimum version number

```php
protected set_versionMin(int $version): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |





***

### set_versionMax

sets the maximum version number

```php
protected set_versionMax(int $version): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |





***

### set_eccLevel

sets the error correction level

```php
protected set_eccLevel(int $eccLevel): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eccLevel` | **int** |  |




**Throws:**

- [`QRCodeException`](./QRCodeException.md)



***

### set_maskPattern

sets/clamps the mask pattern

```php
protected set_maskPattern(int $maskPattern): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maskPattern` | **int** |  |





***

### set_imageTransparencyBG

sets the transparency background color

```php
protected set_imageTransparencyBG(array $imageTransparencyBG): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$imageTransparencyBG` | **array** |  |




**Throws:**

- [`QRCodeException`](./QRCodeException.md)



***

### set_version

sets/clamps the version number

```php
protected set_version(int $version): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |





***

### set_fpdfMeasureUnit

sets the FPDF measurement unit

```php
protected set_fpdfMeasureUnit(string $unit): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$unit` | **string** |  |





***

***
> Automatically generated on 2025-03-18

