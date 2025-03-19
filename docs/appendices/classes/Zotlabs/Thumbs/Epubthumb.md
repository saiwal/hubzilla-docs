
# Epubthumb

Thumbnail creation for epub files.



* Full name: `\Zotlabs\Thumbs\Epubthumb`




## Methods


### Match

Match for application/epub+zip.

```php
public Match(string $type): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | MimeType |





***

### Thumb

Create the thumbnail if the Epub has a cover.

```php
public Thumb(array $attach, int $preview_style, int $height = 300, int $width = 300): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attach` | **array** |  |
| `$preview_style` | **int** | unused |
| `$height` | **int** | (optional) default 300 |
| `$width` | **int** | (optional) default 300 |





***

### getCoverFromEpub

Fetch the cover from the epub archive, if it's present.

```php
private getCoverFromEpub(string $filename): \GdImage|false
```

There's a few limitations here: This will only work if the cover
is a raster image of a supported format. SVG does not work, neither
will other schemes sometimes used for cover/front page.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** | The local filename of the epub archive. |


**Return Value:**

If a cover is found, it is returned as a
GdImage object. Otherwise return false.




***

### parseEpub

Parse the epub to find the path of the cover image.

```php
private parseEpub(\ZipArchive $epub): string|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$epub` | **\ZipArchive** | An opened epub ZipArchive. |


**Return Value:**

The path to the cover image or false.




***

### getEpubPackagePath

Locate the package file within the epub.

```php
private getEpubPackagePath(\ZipArchive $epub): string|false
```

The package file in an epub archive contains the manifest
that again may contain a reference to the cover for the
epub.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$epub` | **\ZipArchive** | An opened epub archive. |


**Return Value:**

The full pathname of the package file or false.




***


***
> Automatically generated on 2025-03-19
