
# ImagickDraw





* Full name: `\ImagickDraw`

**See Also:**

* https://php.net/manual/en/class.imagickdraw.php - 




## Methods


### resetVectorGraphics



```php
public resetVectorGraphics(): mixed
```












***

### getTextKerning



```php
public getTextKerning(): mixed
```












***

### setTextKerning



```php
public setTextKerning(mixed $kerning): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$kerning` | **mixed** |  |





***

### getTextInterWordSpacing



```php
public getTextInterWordSpacing(): mixed
```












***

### setTextInterWordSpacing



```php
public setTextInterWordSpacing(mixed $spacing): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$spacing` | **mixed** |  |





***

### getTextInterLineSpacing



```php
public getTextInterLineSpacing(): mixed
```












***

### setTextInterLineSpacing



```php
public setTextInterLineSpacing(mixed $spacing): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$spacing` | **mixed** |  |





***

### __construct

(PECL imagick 2.0.0)<br/>
The ImagickDraw constructor

```php
public __construct(): mixed
```












**See Also:**

* https://php.net/manual/en/imagickdraw.construct.php - 

***

### setFillColor

(PECL imagick 2.0.0)<br/>
Sets the fill color to be used for drawing filled objects

```php
public setFillColor(\ImagickPixel $fill_pixel): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fill_pixel` | **\ImagickPixel** | &lt;p&gt;<br />ImagickPixel to use to set the color<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfillcolor.php - 

***

### setFillAlpha

(PECL imagick 2.0.0)<br/>
Sets the opacity to use when drawing using the fill color or fill texture

```php
public setFillAlpha(float $opacity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$opacity` | **float** | &lt;p&gt;<br />fill alpha<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfillalpha.php - 

***

### setResolution



```php
public setResolution(mixed $x_resolution, mixed $y_resolution): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_resolution` | **mixed** |  |
| `$y_resolution` | **mixed** |  |





***

### setStrokeColor

(PECL imagick 2.0.0)<br/>
Sets the color used for stroking object outlines

```php
public setStrokeColor(\ImagickPixel $stroke_pixel): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stroke_pixel` | **\ImagickPixel** | &lt;p&gt;<br />the stroke color<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokecolor.php - 

***

### setStrokeAlpha

(PECL imagick 2.0.0)<br/>
Specifies the opacity of stroked object outlines

```php
public setStrokeAlpha(float $opacity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$opacity` | **float** | &lt;p&gt;<br />opacity<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokealpha.php - 

***

### setStrokeWidth

(PECL imagick 2.0.0)<br/>
Sets the width of the stroke used to draw object outlines

```php
public setStrokeWidth(float $stroke_width): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stroke_width` | **float** | &lt;p&gt;<br />stroke width<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokewidth.php - 

***

### clear

(PECL imagick 2.0.0)<br/>
Clears the ImagickDraw

```php
public clear(): bool
```









**Return Value:**

an ImagickDraw object.




**See Also:**

* https://php.net/manual/en/imagickdraw.clear.php - 

***

### circle

(PECL imagick 2.0.0)<br/>
Draws a circle

```php
public circle(float $ox, float $oy, float $px, float $py): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ox` | **float** | &lt;p&gt;<br />origin x coordinate<br />&lt;/p&gt; |
| `$oy` | **float** | &lt;p&gt;<br />origin y coordinate<br />&lt;/p&gt; |
| `$px` | **float** | &lt;p&gt;<br />perimeter x coordinate<br />&lt;/p&gt; |
| `$py` | **float** | &lt;p&gt;<br />perimeter y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.circle.php - 

***

### annotation

(PECL imagick 2.0.0)<br/>
Draws text on the image

```php
public annotation(float $x, float $y, string $text): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />The x coordinate where text is drawn<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />The y coordinate where text is drawn<br />&lt;/p&gt; |
| `$text` | **string** | &lt;p&gt;<br />The text to draw on the image<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.annotation.php - 

***

### setTextAntialias

(PECL imagick 2.0.0)<br/>
Controls whether text is antialiased

```php
public setTextAntialias(bool $antiAlias): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$antiAlias` | **bool** |  |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.settextantialias.php - 

***

### setTextEncoding

(PECL imagick 2.0.0)<br/>
Specifies specifies the text code set

```php
public setTextEncoding(string $encoding): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **string** | &lt;p&gt;<br />the encoding name<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.settextencoding.php - 

***

### setFont

(PECL imagick 2.0.0)<br/>
Sets the fully-specified font to use when annotating with text

```php
public setFont(string $font_name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$font_name` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfont.php - 

***

### setFontFamily

(PECL imagick 2.0.0)<br/>
Sets the font family to use when annotating with text

```php
public setFontFamily(string $font_family): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$font_family` | **string** | &lt;p&gt;<br />the font family<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfontfamily.php - 

***

### setFontSize

(PECL imagick 2.0.0)<br/>
Sets the font pointsize to use when annotating with text

```php
public setFontSize(float $pointsize): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pointsize` | **float** | &lt;p&gt;<br />the point size<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfontsize.php - 

***

### setFontStyle

(PECL imagick 2.0.0)<br/>
Sets the font style to use when annotating with text

```php
public setFontStyle(int $style): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$style` | **int** | &lt;p&gt;<br />STYLETYPE_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfontstyle.php - 

***

### setFontWeight

(PECL imagick 2.0.0)<br/>
Sets the font weight

```php
public setFontWeight(int $font_weight): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$font_weight` | **int** |  |





**See Also:**

* https://php.net/manual/en/imagickdraw.setfontweight.php - 

***

### getFont

(PECL imagick 2.0.0)<br/>
Returns the font

```php
public getFont(): string|false
```









**Return Value:**

a string on success and false if no font is set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getfont.php - 

***

### getFontFamily

(PECL imagick 2.0.0)<br/>
Returns the font family

```php
public getFontFamily(): string|false
```









**Return Value:**

the font family currently selected or false if font family is not set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getfontfamily.php - 

***

### getFontSize

(PECL imagick 2.0.0)<br/>
Returns the font pointsize

```php
public getFontSize(): float
```









**Return Value:**

the font size associated with the current ImagickDraw object.




**See Also:**

* https://php.net/manual/en/imagickdraw.getfontsize.php - 

***

### getFontStyle

(PECL imagick 2.0.0)<br/>
Returns the font style

```php
public getFontStyle(): int
```









**Return Value:**

the font style constant (STYLE_) associated with the ImagickDraw object
or 0 if no style is set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getfontstyle.php - 

***

### getFontWeight

(PECL imagick 2.0.0)<br/>
Returns the font weight

```php
public getFontWeight(): int
```









**Return Value:**

an int on success and 0 if no weight is set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getfontweight.php - 

***

### destroy

(PECL imagick 2.0.0)<br/>
Frees all associated resources

```php
public destroy(): bool
```









**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.destroy.php - 

***

### rectangle

(PECL imagick 2.0.0)<br/>
Draws a rectangle

```php
public rectangle(float $x1, float $y1, float $x2, float $y2): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x1` | **float** | &lt;p&gt;<br />x coordinate of the top left corner<br />&lt;/p&gt; |
| `$y1` | **float** | &lt;p&gt;<br />y coordinate of the top left corner<br />&lt;/p&gt; |
| `$x2` | **float** | &lt;p&gt;<br />x coordinate of the bottom right corner<br />&lt;/p&gt; |
| `$y2` | **float** | &lt;p&gt;<br />y coordinate of the bottom right corner<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.rectangle.php - 

***

### roundRectangle

(PECL imagick 2.0.0)<br/>
Draws a rounded rectangle

```php
public roundRectangle(float $x1, float $y1, float $x2, float $y2, float $rx, float $ry): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x1` | **float** | &lt;p&gt;<br />x coordinate of the top left corner<br />&lt;/p&gt; |
| `$y1` | **float** | &lt;p&gt;<br />y coordinate of the top left corner<br />&lt;/p&gt; |
| `$x2` | **float** | &lt;p&gt;<br />x coordinate of the bottom right<br />&lt;/p&gt; |
| `$y2` | **float** | &lt;p&gt;<br />y coordinate of the bottom right<br />&lt;/p&gt; |
| `$rx` | **float** | &lt;p&gt;<br />x rounding<br />&lt;/p&gt; |
| `$ry` | **float** | &lt;p&gt;<br />y rounding<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.roundrectangle.php - 

***

### ellipse

(PECL imagick 2.0.0)<br/>
Draws an ellipse on the image

```php
public ellipse(float $ox, float $oy, float $rx, float $ry, float $start, float $end): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ox` | **float** |  |
| `$oy` | **float** |  |
| `$rx` | **float** |  |
| `$ry` | **float** |  |
| `$start` | **float** |  |
| `$end` | **float** |  |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.ellipse.php - 

***

### skewX

(PECL imagick 2.0.0)<br/>
Skews the current coordinate system in the horizontal direction

```php
public skewX(float $degrees): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$degrees` | **float** | &lt;p&gt;<br />degrees to skew<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.skewx.php - 

***

### skewY

(PECL imagick 2.0.0)<br/>
Skews the current coordinate system in the vertical direction

```php
public skewY(float $degrees): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$degrees` | **float** | &lt;p&gt;<br />degrees to skew<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.skewy.php - 

***

### translate

(PECL imagick 2.0.0)<br/>
Applies a translation to the current coordinate system

```php
public translate(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />horizontal translation<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />vertical translation<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.translate.php - 

***

### line

(PECL imagick 2.0.0)<br/>
Draws a line

```php
public line(float $sx, float $sy, float $ex, float $ey): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sx` | **float** | &lt;p&gt;<br />starting x coordinate<br />&lt;/p&gt; |
| `$sy` | **float** | &lt;p&gt;<br />starting y coordinate<br />&lt;/p&gt; |
| `$ex` | **float** | &lt;p&gt;<br />ending x coordinate<br />&lt;/p&gt; |
| `$ey` | **float** | &lt;p&gt;<br />ending y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.line.php - 

***

### arc

(PECL imagick 2.0.0)<br/>
Draws an arc

```php
public arc(float $sx, float $sy, float $ex, float $ey, float $sd, float $ed): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sx` | **float** | &lt;p&gt;<br />Starting x ordinate of bounding rectangle<br />&lt;/p&gt; |
| `$sy` | **float** | &lt;p&gt;<br />starting y ordinate of bounding rectangle<br />&lt;/p&gt; |
| `$ex` | **float** | &lt;p&gt;<br />ending x ordinate of bounding rectangle<br />&lt;/p&gt; |
| `$ey` | **float** | &lt;p&gt;<br />ending y ordinate of bounding rectangle<br />&lt;/p&gt; |
| `$sd` | **float** | &lt;p&gt;<br />starting degrees of rotation<br />&lt;/p&gt; |
| `$ed` | **float** | &lt;p&gt;<br />ending degrees of rotation<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.arc.php - 

***

### matte

(PECL imagick 2.0.0)<br/>
Paints on the image's opacity channel

```php
public matte(float $x, float $y, int $paintMethod): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the matte<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the matte<br />&lt;/p&gt; |
| `$paintMethod` | **int** | &lt;p&gt;<br />PAINT_ constant<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.matte.php - 

***

### polygon

(PECL imagick 2.0.0)<br/>
Draws a polygon

```php
public polygon(array $coordinates): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$coordinates` | **array** | &lt;p&gt;<br />multidimensional array like array( array( &#039;x&#039; =&gt; 3, &#039;y&#039; =&gt; 4 ), array( &#039;x&#039; =&gt; 2, &#039;y&#039; =&gt; 6 ) );<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickdraw.polygon.php - 

***

### point

(PECL imagick 2.0.0)<br/>
Draws a point

```php
public point(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />point&#039;s x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />point&#039;s y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.point.php - 

***

### getTextDecoration

(PECL imagick 2.0.0)<br/>
Returns the text decoration

```php
public getTextDecoration(): int
```









**Return Value:**

one of the DECORATION_ constants
and 0 if no decoration is set.




**See Also:**

* https://php.net/manual/en/imagickdraw.gettextdecoration.php - 

***

### getTextEncoding

(PECL imagick 2.0.0)<br/>
Returns the code set used for text annotations

```php
public getTextEncoding(): string
```









**Return Value:**

a string specifying the code set
or false if text encoding is not set.




**See Also:**

* https://php.net/manual/en/imagickdraw.gettextencoding.php - 

***

### getFontStretch



```php
public getFontStretch(): mixed
```












***

### setFontStretch

(PECL imagick 2.0.0)<br/>
Sets the font stretch to use when annotating with text

```php
public setFontStretch(int $fontStretch): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fontStretch` | **int** | &lt;p&gt;<br />STRETCH_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfontstretch.php - 

***

### setStrokeAntialias

(PECL imagick 2.0.0)<br/>
Controls whether stroked outlines are antialiased

```php
public setStrokeAntialias(bool $stroke_antialias): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stroke_antialias` | **bool** | &lt;p&gt;<br />the antialias setting<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokeantialias.php - 

***

### setTextAlignment

(PECL imagick 2.0.0)<br/>
Specifies a text alignment

```php
public setTextAlignment(int $alignment): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$alignment` | **int** | &lt;p&gt;<br />ALIGN_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.settextalignment.php - 

***

### setTextDecoration

(PECL imagick 2.0.0)<br/>
Specifies a decoration

```php
public setTextDecoration(int $decoration): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$decoration` | **int** | &lt;p&gt;<br />DECORATION_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.settextdecoration.php - 

***

### setTextUnderColor

(PECL imagick 2.0.0)<br/>
Specifies the color of a background rectangle

```php
public setTextUnderColor(\ImagickPixel $under_color): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$under_color` | **\ImagickPixel** | &lt;p&gt;<br />the under color<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.settextundercolor.php - 

***

### setViewbox

(PECL imagick 2.0.0)<br/>
Sets the overall canvas size

```php
public setViewbox(int $x1, int $y1, int $x2, int $y2): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x1` | **int** | &lt;p&gt;<br />left x coordinate<br />&lt;/p&gt; |
| `$y1` | **int** | &lt;p&gt;<br />left y coordinate<br />&lt;/p&gt; |
| `$x2` | **int** | &lt;p&gt;<br />right x coordinate<br />&lt;/p&gt; |
| `$y2` | **int** | &lt;p&gt;<br />right y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setviewbox.php - 

***

### affine

(PECL imagick 2.0.0)<br/>
Adjusts the current affine transformation matrix

```php
public affine(array $affine): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$affine` | **array** | &lt;p&gt;<br />Affine matrix parameters<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.affine.php - 

***

### bezier

(PECL imagick 2.0.0)<br/>
Draws a bezier curve

```php
public bezier(array $coordinates): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$coordinates` | **array** | &lt;p&gt;<br />Multidimensional array like array( array( &#039;x&#039; =&gt; 1, &#039;y&#039; =&gt; 2 ),<br />array( &#039;x&#039; =&gt; 3, &#039;y&#039; =&gt; 4 ) )<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.bezier.php - 

***

### composite

(PECL imagick 2.0.0)<br/>
Composites an image onto the current image

```php
public composite(int $compose, float $x, float $y, float $width, float $height, \Imagick $compositeWand): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compose` | **int** | &lt;p&gt;<br />composition operator. One of COMPOSITE_ constants<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the top left corner<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the top left corner<br />&lt;/p&gt; |
| `$width` | **float** | &lt;p&gt;<br />width of the composition image<br />&lt;/p&gt; |
| `$height` | **float** | &lt;p&gt;<br />height of the composition image<br />&lt;/p&gt; |
| `$compositeWand` | **\Imagick** | &lt;p&gt;<br />the Imagick object where composition image is taken from<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickdraw.composite.php - 

***

### color

(PECL imagick 2.0.0)<br/>
Draws color on image

```php
public color(float $x, float $y, int $paintMethod): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the paint<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the paint<br />&lt;/p&gt; |
| `$paintMethod` | **int** | &lt;p&gt;<br />one of the PAINT_ constants<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.color.php - 

***

### comment

(PECL imagick 2.0.0)<br/>
Adds a comment

```php
public comment(string $comment): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$comment` | **string** | &lt;p&gt;<br />The comment string to add to vector output stream<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.comment.php - 

***

### getClipPath

(PECL imagick 2.0.0)<br/>
Obtains the current clipping path ID

```php
public getClipPath(): string|false
```









**Return Value:**

a string containing the clip path ID or false if no clip path exists.




**See Also:**

* https://php.net/manual/en/imagickdraw.getclippath.php - 

***

### getClipRule

(PECL imagick 2.0.0)<br/>
Returns the current polygon fill rule

```php
public getClipRule(): int
```









**Return Value:**

one of the FILLRULE_ constants.




**See Also:**

* https://php.net/manual/en/imagickdraw.getcliprule.php - 

***

### getClipUnits

(PECL imagick 2.0.0)<br/>
Returns the interpretation of clip path units

```php
public getClipUnits(): int
```









**Return Value:**

an int on success.




**See Also:**

* https://php.net/manual/en/imagickdraw.getclipunits.php - 

***

### getFillColor

(PECL imagick 2.0.0)<br/>
Returns the fill color

```php
public getFillColor(): \ImagickPixel
```









**Return Value:**

an ImagickPixel object.




**See Also:**

* https://php.net/manual/en/imagickdraw.getfillcolor.php - 

***

### getFillOpacity

(PECL imagick 2.0.0)<br/>
Returns the opacity used when drawing

```php
public getFillOpacity(): float
```









**Return Value:**

The opacity.




**See Also:**

* https://php.net/manual/en/imagickdraw.getfillopacity.php - 

***

### getFillRule

(PECL imagick 2.0.0)<br/>
Returns the fill rule

```php
public getFillRule(): int
```









**Return Value:**

a FILLRULE_ constant




**See Also:**

* https://php.net/manual/en/imagickdraw.getfillrule.php - 

***

### getGravity

(PECL imagick 2.0.0)<br/>
Returns the text placement gravity

```php
public getGravity(): int
```









**Return Value:**

a GRAVITY_ constant on success and 0 if no gravity is set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getgravity.php - 

***

### getStrokeAntialias

(PECL imagick 2.0.0)<br/>
Returns the current stroke antialias setting

```php
public getStrokeAntialias(): bool
```









**Return Value:**

<b>TRUE</b> if antialiasing is on and false if it is off.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokeantialias.php - 

***

### getStrokeColor

(PECL imagick 2.0.0)<br/>
Returns the color used for stroking object outlines

```php
public getStrokeColor(): \ImagickPixel
```









**Return Value:**

an ImagickPixel object which describes the color.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokecolor.php - 

***

### getStrokeDashArray

(PECL imagick 2.0.0)<br/>
Returns an array representing the pattern of dashes and gaps used to stroke paths

```php
public getStrokeDashArray(): array
```









**Return Value:**

an array on success and empty array if not set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokedasharray.php - 

***

### getStrokeDashOffset

(PECL imagick 2.0.0)<br/>
Returns the offset into the dash pattern to start the dash

```php
public getStrokeDashOffset(): float
```









**Return Value:**

a float representing the offset and 0 if it's not set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokedashoffset.php - 

***

### getStrokeLineCap

(PECL imagick 2.0.0)<br/>
Returns the shape to be used at the end of open subpaths when they are stroked

```php
public getStrokeLineCap(): int
```









**Return Value:**

one of the LINECAP_ constants or 0 if stroke linecap is not set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokelinecap.php - 

***

### getStrokeLineJoin

(PECL imagick 2.0.0)<br/>
Returns the shape to be used at the corners of paths when they are stroked

```php
public getStrokeLineJoin(): int
```









**Return Value:**

one of the LINEJOIN_ constants or 0 if stroke line join is not set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokelinejoin.php - 

***

### getStrokeMiterLimit

(PECL imagick 2.0.0)<br/>
Returns the stroke miter limit

```php
public getStrokeMiterLimit(): int
```









**Return Value:**

an int describing the miter limit
and 0 if no miter limit is set.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokemiterlimit.php - 

***

### getStrokeOpacity

(PECL imagick 2.0.0)<br/>
Returns the opacity of stroked object outlines

```php
public getStrokeOpacity(): float
```









**Return Value:**

a float describing the opacity.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokeopacity.php - 

***

### getStrokeWidth

(PECL imagick 2.0.0)<br/>
Returns the width of the stroke used to draw object outlines

```php
public getStrokeWidth(): float
```









**Return Value:**

a float describing the stroke width.




**See Also:**

* https://php.net/manual/en/imagickdraw.getstrokewidth.php - 

***

### getTextAlignment

(PECL imagick 2.0.0)<br/>
Returns the text alignment

```php
public getTextAlignment(): int
```









**Return Value:**

one of the ALIGN_ constants and 0 if no align is set.




**See Also:**

* https://php.net/manual/en/imagickdraw.gettextalignment.php - 

***

### getTextAntialias

(PECL imagick 2.0.0)<br/>
Returns the current text antialias setting

```php
public getTextAntialias(): bool
```









**Return Value:**

<b>TRUE</b> if text is antialiased and false if not.




**See Also:**

* https://php.net/manual/en/imagickdraw.gettextantialias.php - 

***

### getVectorGraphics

(PECL imagick 2.0.0)<br/>
Returns a string containing vector graphics

```php
public getVectorGraphics(): string
```









**Return Value:**

a string containing the vector graphics.




**See Also:**

* https://php.net/manual/en/imagickdraw.getvectorgraphics.php - 

***

### getTextUnderColor

(PECL imagick 2.0.0)<br/>
Returns the text under color

```php
public getTextUnderColor(): \ImagickPixel
```









**Return Value:**

an ImagickPixel object describing the color.




**See Also:**

* https://php.net/manual/en/imagickdraw.gettextundercolor.php - 

***

### pathClose

(PECL imagick 2.0.0)<br/>
Adds a path element to the current path

```php
public pathClose(): bool
```









**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathclose.php - 

***

### pathCurveToAbsolute

(PECL imagick 2.0.0)<br/>
Draws a cubic Bezier curve

```php
public pathCurveToAbsolute(float $x1, float $y1, float $x2, float $y2, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x1` | **float** | &lt;p&gt;<br />x coordinate of the first control point<br />&lt;/p&gt; |
| `$y1` | **float** | &lt;p&gt;<br />y coordinate of the first control point<br />&lt;/p&gt; |
| `$x2` | **float** | &lt;p&gt;<br />x coordinate of the second control point<br />&lt;/p&gt; |
| `$y2` | **float** | &lt;p&gt;<br />y coordinate of the first control point<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the curve end<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the curve end<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetoabsolute.php - 

***

### pathCurveToRelative

(PECL imagick 2.0.0)<br/>
Draws a cubic Bezier curve

```php
public pathCurveToRelative(float $x1, float $y1, float $x2, float $y2, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x1` | **float** | &lt;p&gt;<br />x coordinate of starting control point<br />&lt;/p&gt; |
| `$y1` | **float** | &lt;p&gt;<br />y coordinate of starting control point<br />&lt;/p&gt; |
| `$x2` | **float** | &lt;p&gt;<br />x coordinate of ending control point<br />&lt;/p&gt; |
| `$y2` | **float** | &lt;p&gt;<br />y coordinate of ending control point<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />ending x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />ending y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetorelative.php - 

***

### pathCurveToQuadraticBezierAbsolute

(PECL imagick 2.0.0)<br/>
Draws a quadratic Bezier curve

```php
public pathCurveToQuadraticBezierAbsolute(float $x1, float $y1, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x1` | **float** | &lt;p&gt;<br />x coordinate of the control point<br />&lt;/p&gt; |
| `$y1` | **float** | &lt;p&gt;<br />y coordinate of the control point<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the end point<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the end point<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetoquadraticbezierabsolute.php - 

***

### pathCurveToQuadraticBezierRelative

(PECL imagick 2.0.0)<br/>
Draws a quadratic Bezier curve

```php
public pathCurveToQuadraticBezierRelative(float $x1, float $y1, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x1` | **float** | &lt;p&gt;<br />starting x coordinate<br />&lt;/p&gt; |
| `$y1` | **float** | &lt;p&gt;<br />starting y coordinate<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />ending x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />ending y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetoquadraticbezierrelative.php - 

***

### pathCurveToQuadraticBezierSmoothAbsolute

(PECL imagick 2.0.0)<br/>
Draws a quadratic Bezier curve

```php
public pathCurveToQuadraticBezierSmoothAbsolute(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />ending x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />ending y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetoquadraticbeziersmoothabsolute.php - 

***

### pathCurveToQuadraticBezierSmoothRelative

(PECL imagick 2.0.0)<br/>
Draws a quadratic Bezier curve

```php
public pathCurveToQuadraticBezierSmoothRelative(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />ending x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />ending y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetoquadraticbeziersmoothrelative.php - 

***

### pathCurveToSmoothAbsolute

(PECL imagick 2.0.0)<br/>
Draws a cubic Bezier curve

```php
public pathCurveToSmoothAbsolute(float $x2, float $y2, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x2` | **float** | &lt;p&gt;<br />x coordinate of the second control point<br />&lt;/p&gt; |
| `$y2` | **float** | &lt;p&gt;<br />y coordinate of the second control point<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the ending point<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the ending point<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetosmoothabsolute.php - 

***

### pathCurveToSmoothRelative

(PECL imagick 2.0.0)<br/>
Draws a cubic Bezier curve

```php
public pathCurveToSmoothRelative(float $x2, float $y2, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x2` | **float** | &lt;p&gt;<br />x coordinate of the second control point<br />&lt;/p&gt; |
| `$y2` | **float** | &lt;p&gt;<br />y coordinate of the second control point<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the ending point<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the ending point<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathcurvetosmoothrelative.php - 

***

### pathEllipticArcAbsolute

(PECL imagick 2.0.0)<br/>
Draws an elliptical arc

```php
public pathEllipticArcAbsolute(float $rx, float $ry, float $x_axis_rotation, bool $large_arc_flag, bool $sweep_flag, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rx` | **float** | &lt;p&gt;<br />x radius<br />&lt;/p&gt; |
| `$ry` | **float** | &lt;p&gt;<br />y radius<br />&lt;/p&gt; |
| `$x_axis_rotation` | **float** | &lt;p&gt;<br />x axis rotation<br />&lt;/p&gt; |
| `$large_arc_flag` | **bool** | &lt;p&gt;<br />large arc flag<br />&lt;/p&gt; |
| `$sweep_flag` | **bool** | &lt;p&gt;<br />sweep flag<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathellipticarcabsolute.php - 

***

### pathEllipticArcRelative

(PECL imagick 2.0.0)<br/>
Draws an elliptical arc

```php
public pathEllipticArcRelative(float $rx, float $ry, float $x_axis_rotation, bool $large_arc_flag, bool $sweep_flag, float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rx` | **float** | &lt;p&gt;<br />x radius<br />&lt;/p&gt; |
| `$ry` | **float** | &lt;p&gt;<br />y radius<br />&lt;/p&gt; |
| `$x_axis_rotation` | **float** | &lt;p&gt;<br />x axis rotation<br />&lt;/p&gt; |
| `$large_arc_flag` | **bool** | &lt;p&gt;<br />large arc flag<br />&lt;/p&gt; |
| `$sweep_flag` | **bool** | &lt;p&gt;<br />sweep flag<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathellipticarcrelative.php - 

***

### pathFinish

(PECL imagick 2.0.0)<br/>
Terminates the current path

```php
public pathFinish(): bool
```









**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathfinish.php - 

***

### pathLineToAbsolute

(PECL imagick 2.0.0)<br/>
Draws a line path

```php
public pathLineToAbsolute(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />starting x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />ending x coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathlinetoabsolute.php - 

***

### pathLineToRelative

(PECL imagick 2.0.0)<br/>
Draws a line path

```php
public pathLineToRelative(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />starting x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />starting y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathlinetorelative.php - 

***

### pathLineToHorizontalAbsolute

(PECL imagick 2.0.0)<br/>
Draws a horizontal line path

```php
public pathLineToHorizontalAbsolute(float $x): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />x coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathlinetohorizontalabsolute.php - 

***

### pathLineToHorizontalRelative

(PECL imagick 2.0.0)<br/>
Draws a horizontal line

```php
public pathLineToHorizontalRelative(float $x): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />x coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathlinetohorizontalrelative.php - 

***

### pathLineToVerticalAbsolute

(PECL imagick 2.0.0)<br/>
Draws a vertical line

```php
public pathLineToVerticalAbsolute(float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$y` | **float** | &lt;p&gt;<br />y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathlinetoverticalabsolute.php - 

***

### pathLineToVerticalRelative

(PECL imagick 2.0.0)<br/>
Draws a vertical line path

```php
public pathLineToVerticalRelative(float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$y` | **float** | &lt;p&gt;<br />y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathlinetoverticalrelative.php - 

***

### pathMoveToAbsolute

(PECL imagick 2.0.0)<br/>
Starts a new sub-path

```php
public pathMoveToAbsolute(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the starting point<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the starting point<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathmovetoabsolute.php - 

***

### pathMoveToRelative

(PECL imagick 2.0.0)<br/>
Starts a new sub-path

```php
public pathMoveToRelative(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />target x coordinate<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />target y coordinate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathmovetorelative.php - 

***

### pathStart

(PECL imagick 2.0.0)<br/>
Declares the start of a path drawing list

```php
public pathStart(): bool
```









**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pathstart.php - 

***

### polyline

(PECL imagick 2.0.0)<br/>
Draws a polyline

```php
public polyline(array $coordinates): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$coordinates` | **array** | &lt;p&gt;<br />array of x and y coordinates: array( array( &#039;x&#039; =&gt; 4, &#039;y&#039; =&gt; 6 ), array( &#039;x&#039; =&gt; 8, &#039;y&#039; =&gt; 10 ) )<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickdraw.polyline.php - 

***

### popClipPath

(PECL imagick 2.0.0)<br/>
Terminates a clip path definition

```php
public popClipPath(): bool
```









**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.popclippath.php - 

***

### popDefs

(PECL imagick 2.0.0)<br/>
Terminates a definition list

```php
public popDefs(): bool
```









**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.popdefs.php - 

***

### popPattern

(PECL imagick 2.0.0)<br/>
Terminates a pattern definition

```php
public popPattern(): bool
```









**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.poppattern.php - 

***

### pushClipPath

(PECL imagick 2.0.0)<br/>
Starts a clip path definition

```php
public pushClipPath(string $clip_mask_id): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clip_mask_id` | **string** | &lt;p&gt;<br />Clip mask Id<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pushclippath.php - 

***

### pushDefs

(PECL imagick 2.0.0)<br/>
Indicates that following commands create named elements for early processing

```php
public pushDefs(): bool
```









**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.pushdefs.php - 

***

### pushPattern

(PECL imagick 2.0.0)<br/>
Indicates that subsequent commands up to a ImagickDraw::opPattern() command comprise the definition of a named pattern

```php
public pushPattern(string $pattern_id, float $x, float $y, float $width, float $height): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pattern_id` | **string** | &lt;p&gt;<br />the pattern Id<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />x coordinate of the top-left corner<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />y coordinate of the top-left corner<br />&lt;/p&gt; |
| `$width` | **float** | &lt;p&gt;<br />width of the pattern<br />&lt;/p&gt; |
| `$height` | **float** | &lt;p&gt;<br />height of the pattern<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.pushpattern.php - 

***

### render

(PECL imagick 2.0.0)<br/>
Renders all preceding drawing commands onto the image

```php
public render(): bool
```









**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.render.php - 

***

### rotate

(PECL imagick 2.0.0)<br/>
Applies the specified rotation to the current coordinate space

```php
public rotate(float $degrees): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$degrees` | **float** | &lt;p&gt;<br />degrees to rotate<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.rotate.php - 

***

### scale

(PECL imagick 2.0.0)<br/>
Adjusts the scaling factor

```php
public scale(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** | &lt;p&gt;<br />horizontal factor<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />vertical factor<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.scale.php - 

***

### setClipPath

(PECL imagick 2.0.0)<br/>
Associates a named clipping path with the image

```php
public setClipPath(string $clip_mask): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clip_mask` | **string** | &lt;p&gt;<br />the clipping path name<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setclippath.php - 

***

### setClipRule

(PECL imagick 2.0.0)<br/>
Set the polygon fill rule to be used by the clipping path

```php
public setClipRule(int $fill_rule): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fill_rule` | **int** | &lt;p&gt;<br />FILLRULE_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setcliprule.php - 

***

### setClipUnits

(PECL imagick 2.0.0)<br/>
Sets the interpretation of clip path units

```php
public setClipUnits(int $clip_units): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clip_units` | **int** | &lt;p&gt;<br />the number of clip units<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setclipunits.php - 

***

### setFillOpacity

(PECL imagick 2.0.0)<br/>
Sets the opacity to use when drawing using the fill color or fill texture

```php
public setFillOpacity(float $fillOpacity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fillOpacity` | **float** | &lt;p&gt;<br />the fill opacity<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfillopacity.php - 

***

### setFillPatternURL

(PECL imagick 2.0.0)<br/>
Sets the URL to use as a fill pattern for filling objects

```php
public setFillPatternURL(string $fill_url): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fill_url` | **string** | &lt;p&gt;<br />URL to use to obtain fill pattern.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfillpatternurl.php - 

***

### setFillRule

(PECL imagick 2.0.0)<br/>
Sets the fill rule to use while drawing polygons

```php
public setFillRule(int $fill_rule): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fill_rule` | **int** | &lt;p&gt;<br />FILLRULE_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setfillrule.php - 

***

### setGravity

(PECL imagick 2.0.0)<br/>
Sets the text placement gravity

```php
public setGravity(int $gravity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$gravity` | **int** | &lt;p&gt;<br />GRAVITY_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setgravity.php - 

***

### setStrokePatternURL

(PECL imagick 2.0.0)<br/>
Sets the pattern used for stroking object outlines

```php
public setStrokePatternURL(string $stroke_url): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stroke_url` | **string** | &lt;p&gt;<br />stroke URL<br />&lt;/p&gt; |


**Return Value:**

imagick.imagickdraw.return.success;




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokepatternurl.php - 

***

### setStrokeDashOffset

(PECL imagick 2.0.0)<br/>
Specifies the offset into the dash pattern to start the dash

```php
public setStrokeDashOffset(float $dash_offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dash_offset` | **float** | &lt;p&gt;<br />dash offset<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokedashoffset.php - 

***

### setStrokeLineCap

(PECL imagick 2.0.0)<br/>
Specifies the shape to be used at the end of open subpaths when they are stroked

```php
public setStrokeLineCap(int $linecap): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$linecap` | **int** | &lt;p&gt;<br />LINECAP_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokelinecap.php - 

***

### setStrokeLineJoin

(PECL imagick 2.0.0)<br/>
Specifies the shape to be used at the corners of paths when they are stroked

```php
public setStrokeLineJoin(int $linejoin): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$linejoin` | **int** | &lt;p&gt;<br />LINEJOIN_ constant<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokelinejoin.php - 

***

### setStrokeMiterLimit

(PECL imagick 2.0.0)<br/>
Specifies the miter limit

```php
public setStrokeMiterLimit(int $miterlimit): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$miterlimit` | **int** | &lt;p&gt;<br />the miter limit<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokemiterlimit.php - 

***

### setStrokeOpacity

(PECL imagick 2.0.0)<br/>
Specifies the opacity of stroked object outlines

```php
public setStrokeOpacity(float $stroke_opacity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stroke_opacity` | **float** | &lt;p&gt;<br />stroke opacity. 1.0 is fully opaque<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokeopacity.php - 

***

### setVectorGraphics

(PECL imagick 2.0.0)<br/>
Sets the vector graphics

```php
public setVectorGraphics(string $xml): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xml` | **string** | &lt;p&gt;<br />xml containing the vector graphics<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.setvectorgraphics.php - 

***

### pop

(PECL imagick 2.0.0)<br/>
Destroys the current ImagickDraw in the stack, and returns to the previously pushed ImagickDraw

```php
public pop(): bool
```









**Return Value:**

<b>TRUE</b> on success and false on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.pop.php - 

***

### push

(PECL imagick 2.0.0)<br/>
Clones the current ImagickDraw and pushes it to the stack

```php
public push(): bool
```









**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagickdraw.push.php - 

***

### setStrokeDashArray

(PECL imagick 2.0.0)<br/>
Specifies the pattern of dashes and gaps used to stroke paths

```php
public setStrokeDashArray(array $dashArray): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dashArray` | **array** | &lt;p&gt;<br />array of floats<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickdraw.setstrokedasharray.php - 

***

### setOpacity

Sets the opacity to use when drawing using the fill or stroke color or texture. Fully opaque is 1.0.

```php
public setOpacity(float $opacity): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$opacity` | **float** |  |





***

### getOpacity

Returns the opacity used when drawing with the fill or stroke color or texture. Fully opaque is 1.0.

```php
public getOpacity(): float
```












***

### setFontResolution

Sets the image font resolution.

```php
public setFontResolution(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** |  |
| `$y` | **float** |  |





***

### getFontResolution

Gets the image X and Y resolution.

```php
public getFontResolution(): array
```












***

### getTextDirection

Returns the direction that will be used when annotating with text.

```php
public getTextDirection(): bool
```












***

### setTextDirection

Sets the font style to use when annotating with text. The AnyStyle enumeration acts as a wild-card "don't care" option.

```php
public setTextDirection(int $direction): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$direction` | **int** |  |





***

### getBorderColor

Returns the border color used for drawing bordered objects.

```php
public getBorderColor(): \ImagickPixel
```












***

### setBorderColor

Sets the border color to be used for drawing bordered objects.

```php
public setBorderColor(\ImagickPixel $color): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **\ImagickPixel** |  |





***

### getDensity

Obtains the vertical and horizontal resolution.

```php
public getDensity(): string|null
```












***

### setDensity

Sets the vertical and horizontal resolution.

```php
public setDensity(string $density_string): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$density_string` | **string** |  |





***


***
> Automatically generated on 2025-03-18
