***

# ImagickPixelIterator





* Full name: `\ImagickPixelIterator`
* This class implements:
[`\Iterator`](./Iterator.md)

**See Also:**

* https://php.net/manual/en/class.imagickpixeliterator.php - 




## Methods


### __construct

(PECL imagick 2.0.0)<br/>
The ImagickPixelIterator constructor

```php
public __construct(\Imagick $wand): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$wand` | **\Imagick** |  |





**See Also:**

* https://php.net/manual/en/imagickpixeliterator.construct.php - 

***

### newPixelIterator

(PECL imagick 2.0.0)<br/>
Returns a new pixel iterator

```php
public newPixelIterator(\Imagick $wand): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$wand` | **\Imagick** |  |


**Return Value:**

<b>TRUE</b> on success. Throwing ImagickPixelIteratorException.



**Throws:**

- [`ImagickPixelIteratorException`](./ImagickPixelIteratorException.md)



**See Also:**

* https://php.net/manual/en/imagickpixeliterator.newpixeliterator.php - 

***

### newPixelRegionIterator

(PECL imagick 2.0.0)<br/>
Returns a new pixel iterator

```php
public newPixelRegionIterator(\Imagick $wand, int $x, int $y, int $columns, int $rows): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$wand` | **\Imagick** |  |
| `$x` | **int** |  |
| `$y` | **int** |  |
| `$columns` | **int** |  |
| `$rows` | **int** |  |


**Return Value:**

a new ImagickPixelIterator on success; on failure, throws ImagickPixelIteratorException



**Throws:**

- [`ImagickPixelIteratorException`](./ImagickPixelIteratorException.md)



**See Also:**

* https://php.net/manual/en/imagickpixeliterator.newpixelregioniterator.php - 

***

### getIteratorRow

(PECL imagick 2.0.0)<br/>
Returns the current pixel iterator row

```php
public getIteratorRow(): int
```









**Return Value:**

the integer offset of the row, throwing ImagickPixelIteratorException on error.



**Throws:**
<p>on error</p>

- [`ImagickPixelIteratorException`](./ImagickPixelIteratorException.md)



**See Also:**

* https://php.net/manual/en/imagickpixeliterator.getiteratorrow.php - 

***

### setIteratorRow

(PECL imagick 2.0.0)<br/>
Set the pixel iterator row

```php
public setIteratorRow(int $row): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$row` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.setiteratorrow.php - 

***

### setIteratorFirstRow

(PECL imagick 2.0.0)<br/>
Sets the pixel iterator to the first pixel row

```php
public setIteratorFirstRow(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.setiteratorfirstrow.php - 

***

### setIteratorLastRow

(PECL imagick 2.0.0)<br/>
Sets the pixel iterator to the last pixel row

```php
public setIteratorLastRow(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.setiteratorlastrow.php - 

***

### getPreviousIteratorRow

(PECL imagick 2.0.0)<br/>
Returns the previous row

```php
public getPreviousIteratorRow(): array
```









**Return Value:**

the previous row as an array of ImagickPixelWand objects from the
ImagickPixelIterator, throwing ImagickPixelIteratorException on error.



**Throws:**
<p>on error</p>

- [`ImagickPixelIteratorException`](./ImagickPixelIteratorException.md)



**See Also:**

* https://php.net/manual/en/imagickpixeliterator.getpreviousiteratorrow.php - 

***

### getCurrentIteratorRow

(PECL imagick 2.0.0)<br/>
Returns the current row of ImagickPixel objects

```php
public getCurrentIteratorRow(): array
```









**Return Value:**

a row as an array of ImagickPixel objects that can themselves be iterated.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.getcurrentiteratorrow.php - 

***

### getNextIteratorRow

(PECL imagick 2.0.0)<br/>
Returns the next row of the pixel iterator

```php
public getNextIteratorRow(): array
```









**Return Value:**

the next row as an array of ImagickPixel objects, throwing
ImagickPixelIteratorException on error.



**Throws:**
<p>on error</p>

- [`ImagickPixelIteratorException`](./ImagickPixelIteratorException.md)



**See Also:**

* https://php.net/manual/en/imagickpixeliterator.getnextiteratorrow.php - 

***

### resetIterator

(PECL imagick 2.0.0)<br/>
Resets the pixel iterator

```php
public resetIterator(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.resetiterator.php - 

***

### syncIterator

(PECL imagick 2.0.0)<br/>
Syncs the pixel iterator

```php
public syncIterator(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.synciterator.php - 

***

### destroy

(PECL imagick 2.0.0)<br/>
Deallocates resources associated with a PixelIterator

```php
public destroy(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.destroy.php - 

***

### clear

(PECL imagick 2.0.0)<br/>
Clear resources associated with a PixelIterator

```php
public clear(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagickpixeliterator.clear.php - 

***

### getpixeliterator



```php
public static getpixeliterator(\Imagick $Imagick): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Imagick` | **\Imagick** |  |





***

### getpixelregioniterator



```php
public static getpixelregioniterator(\Imagick $Imagick, mixed $x, mixed $y, mixed $columns, mixed $rows): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Imagick` | **\Imagick** |  |
| `$x` | **mixed** |  |
| `$y` | **mixed** |  |
| `$columns` | **mixed** |  |
| `$rows` | **mixed** |  |





***

### key



```php
public key(): mixed
```












***

### next



```php
public next(): mixed
```












***

### rewind



```php
public rewind(): mixed
```












***

### current



```php
public current(): mixed
```












***

### valid



```php
public valid(): mixed
```












***


***
> Automatically generated on 2025-03-15
