
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
public Thumb(array $attach, \Zotlabs\Thumbs\number $preview_style, \Zotlabs\Thumbs\number $height = 300, \Zotlabs\Thumbs\number $width = 300): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attach` | **array** |  |
| `$preview_style` | **\Zotlabs\Thumbs\number** | unused |
| `$height` | **\Zotlabs\Thumbs\number** | (optional) default 300 |
| `$width` | **\Zotlabs\Thumbs\number** | (optional) default 300 |





***

### getCover



```php
private getCover(string $filename): \GdImage|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |





***


***
> Automatically generated on 2025-03-15
