
# PhotoImagick





* Full name: `\Zotlabs\Photo\PhotoImagick`
* Parent class: [`\Zotlabs\Photo\PhotoDriver`](./PhotoDriver.md)




## Methods


### supportedTypes



```php
public supportedTypes(): array
```









**Return Value:**


Associative array with mimetype as key and file extension as value.




***

### load



```php
protected load(mixed $data, mixed $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$type` | **mixed** |  |





***

### destroy



```php
protected destroy(): mixed
```












***

### setDimensions



```php
protected setDimensions(): mixed
```












***

### clearexif



```php
public clearexif(): mixed
```












**See Also:**

* \Zotlabs\Photo\PhotoDriver::clearexif() - 

***

### getImage



```php
public getImage(): bool|\Imagick
```












**See Also:**

* \Zotlabs\Photo\PhotoDriver::getImage() - 

***

### doScaleImage



```php
public doScaleImage(mixed $dest_width, mixed $dest_height): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dest_width` | **mixed** |  |
| `$dest_height` | **mixed** |  |





***

### rotate



```php
public rotate(mixed $degrees): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$degrees` | **mixed** |  |





***

### flip



```php
public flip(mixed $horiz = true, mixed $vert = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$horiz` | **mixed** |  |
| `$vert` | **mixed** |  |





***

### cropImageRect



```php
public cropImageRect(mixed $maxx, mixed $maxy, mixed $x, mixed $y, mixed $w, mixed $h): bool|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maxx` | **mixed** | width of the new image |
| `$maxy` | **mixed** | height of the new image |
| `$x` | **mixed** | x-offset for region |
| `$y` | **mixed** | y-offset for region |
| `$w` | **mixed** | width of region |
| `$h` | **mixed** | height of region |


**Return Value:**

false on failure




***

### imageString



```php
public imageString(): string
```









**Return Value:**

A Binary String.




***


## Inherited methods


### supportedTypes



```php
public supportedTypes(): array
```




* This method is **abstract**.




**Return Value:**


Associative array with mimetype as key and file extension as value.




***

### load



```php
protected load(mixed $data, mixed $type): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$type` | **mixed** |  |





***

### destroy



```php
protected destroy(): mixed
```




* This method is **abstract**.







***

### setDimensions



```php
protected setDimensions(): mixed
```




* This method is **abstract**.







***

### getImage



```php
public getImage(): bool|resource|\Imagick
```




* This method is **abstract**.




**Return Value:**


false on failure, a PHP image resource for GD driver, an \Imagick object
for ImageMagick driver.




***

### doScaleImage



```php
public doScaleImage(mixed $new_width, mixed $new_height): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$new_width` | **mixed** |  |
| `$new_height` | **mixed** |  |





***

### rotate



```php
public rotate(mixed $degrees): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$degrees` | **mixed** |  |





***

### flip



```php
public flip(mixed $horiz = true, mixed $vert = false): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$horiz` | **mixed** |  |
| `$vert` | **mixed** |  |





***

### cropImageRect



```php
public cropImageRect(int $maxx, int $maxy, int $x, int $y, int $w, int $h): bool|void
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maxx` | **int** | width of the new image |
| `$maxy` | **int** | height of the new image |
| `$x` | **int** | x-offset for region |
| `$y` | **int** | y-offset for region |
| `$w` | **int** | width of region |
| `$h` | **int** | height of region |


**Return Value:**

false on failure




***

### imageString



```php
public imageString(): string
```




* This method is **abstract**.




**Return Value:**

A Binary String.




***

### clearexif



```php
public clearexif(): mixed
```




* This method is **abstract**.







***

### __construct



```php
public __construct(string $data, string $type = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Image |
| `$type` | **string** | mimetype |





***

### __destruct



```php
public __destruct(): mixed
```












***

### is_valid



```php
public is_valid(): bool
```












***

### getWidth



```php
public getWidth(): bool|\Zotlabs\Photo\number
```









**Return Value:**

Width of image in pixels, or false on failure




***

### getHeight



```php
public getHeight(): bool|\Zotlabs\Photo\number
```









**Return Value:**

Height of image in pixels, or false on failure




***

### saveImage



```php
public saveImage(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** | Path and filename where to save the image |


**Return Value:**

False on failure, otherwise true




***

### getType



```php
public getType(): bool|string
```









**Return Value:**

False on failure, otherwise mimetype.




***

### getExt



```php
public getExt(): bool|string
```









**Return Value:**

False on failure, otherwise file extension.




***

### scaleImage



```php
public scaleImage(int $max, bool $float_height = true): bool|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$max` | **int** | maximum pixel size in either dimension |
| `$float_height` | **bool** | (optional)<br />If true allow height to float to any length on tall images, constraining<br />only the width |


**Return Value:**

false on failure, otherwise void




***

### scaleImageUp



```php
public scaleImageUp(mixed $min): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$min` | **mixed** |  |





***

### scaleImageSquare



```php
public scaleImageSquare(int $dim): bool|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dim` | **int** | Pixel of square image |


**Return Value:**

false on failure, otherwise void




***

### cropImage



```php
public cropImage(int $max, int $x, int $y, int $w, int $h): bool|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$max` | **int** | size of the new image |
| `$x` | **int** | x-offset for region |
| `$y` | **int** | y-offset for region |
| `$w` | **int** | width of region |
| `$h` | **int** | height of region |


**Return Value:**

false on failure




**See Also:**

* \Zotlabs\Photo\cropImageRect() - 

***

### exif



```php
public exif(string $filename): bool|array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |





***

### orient



```php
public orient(array $exif): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exif` | **array** |  |


**Return Value:**

true if oriented, otherwise false




***

### save



```php
public save(array $arr, bool $skipcheck = false): bool|array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** |  |
| `$skipcheck` | **bool** | (optional) default false |





***

### storeThumbnail



```php
public storeThumbnail(array $arr, mixed $scale): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** |  |
| `$scale` | **mixed** |  |





***


***
> Automatically generated on 2025-03-19
