***

# ImagickPixel





* Full name: `\ImagickPixel`

**See Also:**

* https://php.net/manual/en/class.imagickpixel.php - 




## Methods


### getHSL

(PECL imagick 2.0.0)<br/>
Returns the normalized HSL color of the ImagickPixel object

```php
public getHSL(): array
```









**Return Value:**

the HSL value in an array with the keys "hue",
"saturation", and "luminosity". Throws ImagickPixelException on failure.



**Throws:**
<p>on failure</p>

- [`ImagickPixelException`](./ImagickPixelException.md)



**See Also:**

* https://php.net/manual/en/imagickpixel.gethsl.php - 

***

### setHSL

(PECL imagick 2.0.0)<br/>
Sets the normalized HSL color

```php
public setHSL(float $hue, float $saturation, float $luminosity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hue` | **float** | &lt;p&gt;<br />The normalized value for hue, described as a fractional arc<br />(between 0 and 1) of the hue circle, where the zero value is<br />red.<br />&lt;/p&gt; |
| `$saturation` | **float** | &lt;p&gt;<br />The normalized value for saturation, with 1 as full saturation.<br />&lt;/p&gt; |
| `$luminosity` | **float** | &lt;p&gt;<br />The normalized value for luminosity, on a scale from black at<br />0 to white at 1, with the full HS value at 0.5 luminosity.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixel.sethsl.php - 

***

### getColorValueQuantum



```php
public getColorValueQuantum(): mixed
```












***

### setColorValueQuantum



```php
public setColorValueQuantum(mixed $color_value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color_value` | **mixed** |  |





***

### getIndex



```php
public getIndex(): mixed
```












***

### setIndex



```php
public setIndex(mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### __construct

(PECL imagick 2.0.0)<br/>
The ImagickPixel constructor

```php
public __construct(string $color = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **string** | [optional] &lt;p&gt;<br />The optional color string to use as the initial value of this object.<br />&lt;/p&gt; |





**See Also:**

* https://php.net/manual/en/imagickpixel.construct.php - 

***

### setColor

(PECL imagick 2.0.0)<br/>
Sets the color

```php
public setColor(string $color): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **string** | &lt;p&gt;<br />The color definition to use in order to initialise the<br />ImagickPixel object.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> if the specified color was set, <b>FALSE</b> otherwise.




**See Also:**

* https://php.net/manual/en/imagickpixel.setcolor.php - 

***

### setColorValue

(PECL imagick 2.0.0)<br/>
Sets the normalized value of one of the channels

```php
public setColorValue(int $color, float $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **int** | &lt;p&gt;<br />One of the Imagick color constants e.g. \Imagick::COLOR_GREEN or \Imagick::COLOR_ALPHA.<br />&lt;/p&gt; |
| `$value` | **float** | &lt;p&gt;<br />The value to set this channel to, ranging from 0 to 1.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixel.setcolorvalue.php - 

***

### getColorValue

(PECL imagick 2.0.0)<br/>
Gets the normalized value of the provided color channel

```php
public getColorValue(int $color): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **int** | &lt;p&gt;<br />The color to get the value of, specified as one of the Imagick color<br />constants. This can be one of the RGB colors, CMYK colors, alpha and<br />opacity e.g (Imagick::COLOR_BLUE, Imagick::COLOR_MAGENTA).<br />&lt;/p&gt; |


**Return Value:**

The value of the channel, as a normalized floating-point number, throwing
ImagickPixelException on error.



**Throws:**
<p>on error</p>

- [`ImagickPixelException`](./ImagickPixelException.md)



**See Also:**

* https://php.net/manual/en/imagickpixel.getcolorvalue.php - 

***

### clear

(PECL imagick 2.0.0)<br/>
Clears resources associated with this object

```php
public clear(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixel.clear.php - 

***

### destroy

(PECL imagick 2.0.0)<br/>
Deallocates resources associated with this object

```php
public destroy(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixel.destroy.php - 

***

### isSimilar

(PECL imagick 2.0.0)<br/>
Check the distance between this color and another

```php
public isSimilar(\ImagickPixel $color, float $fuzz): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **\ImagickPixel** | &lt;p&gt;<br />The ImagickPixel object to compare this object against.<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The maximum distance within which to consider these colors as similar.<br />The theoretical maximum for this value is the square root of three<br />(1.732).<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixel.issimilar.php - 

***

### isPixelSimilar

(No version information available, might only be in SVN)<br/>
Check the distance between this color and another

```php
public isPixelSimilar(\ImagickPixel $color, float $fuzz): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **\ImagickPixel** | &lt;p&gt;<br />The ImagickPixel object to compare this object against.<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The maximum distance within which to consider these colors as similar.<br />The theoretical maximum for this value is the square root of three<br />(1.732).<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixel.ispixelsimilar.php - 

***

### getColor

(PECL imagick 2.0.0)<br/>
Returns the color

```php
public getColor(bool $normalized = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$normalized` | **bool** | [optional] &lt;p&gt;<br />Normalize the color values<br />&lt;/p&gt; |


**Return Value:**

An array of channel values, each normalized if <b>TRUE</b> is given as param. Throws
ImagickPixelException on error.



**Throws:**
<p>on error.</p>

- [`ImagickPixelException`](./ImagickPixelException.md)



**See Also:**

* https://php.net/manual/en/imagickpixel.getcolor.php - 

***

### getColorAsString

(PECL imagick 2.1.0)<br/>
Returns the color as a string

```php
public getColorAsString(): string
```









**Return Value:**

the color of the ImagickPixel object as a string.




**See Also:**

* https://php.net/manual/en/imagickpixel.getcolorasstring.php - 

***

### getColorCount

(PECL imagick 2.0.0)<br/>
Returns the color count associated with this color

```php
public getColorCount(): int
```









**Return Value:**

the color count as an integer on success, throws
ImagickPixelException on failure.



**Throws:**
<p>on failure.</p>

- [`ImagickPixelException`](./ImagickPixelException.md)



**See Also:**

* https://php.net/manual/en/imagickpixel.getcolorcount.php - 

***

### setColorCount



```php
public setColorCount(mixed $colorCount): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$colorCount` | **mixed** |  |





***

### isPixelSimilarQuantum

Returns true if the distance between two colors is less than the specified distance. The fuzz value should be in the range 0-QuantumRange.<br>
The maximum value represents the longest possible distance in the colorspace. e.g. from RGB(0, 0, 0) to RGB(255, 255, 255) for the RGB colorspace

```php
public isPixelSimilarQuantum(mixed $color, string $fuzz): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **mixed** |  |
| `$fuzz` | **string** |  |





**See Also:**

* https://php.net/manual/en/imagickpixel.ispixelsimilarquantum.php - 

***

### getColorQuantum

Returns the color of the pixel in an array as Quantum values. If ImageMagick was compiled as HDRI these will be floats, otherwise they will be integers.

```php
public getColorQuantum(): mixed
```









**Return Value:**

The quantum value of the color element. Float if ImageMagick was compiled with HDRI, otherwise an int.




**See Also:**

* https://php.net/manual/en/imagickpixel.getcolorquantum.php - 

***

### setColorFromPixel

Sets the color count associated with this color from another ImagickPixel object.

```php
public setColorFromPixel(\ImagickPixel $srcPixel): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$srcPixel` | **\ImagickPixel** |  |





***


***
> Automatically generated on 2025-03-15
