***

# EPubTest

Test for EPUB library

Source: https://github.com/splitbrain/php-epub-meta

* Full name: `\EPubTest`
* Parent class: [`TestCase`](./PHPUnit/Framework/TestCase.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TEST_EPUB`|public| |__DIR__ . &#039;/data/test.epub&#039;|
|`TEST_EPUB_COPY`|public| |__DIR__ . &#039;/data/test.copy.epub&#039;|
|`TEST_EPUB_COVER`|public| |__DIR__ . &#039;/data/test.cover.epub&#039;|
|`TEST_IMAGE`|public| |__DIR__ . &#039;/data/test.jpg&#039;|
|`EMPTY_ZIP`|public| |__DIR__ . &#039;/data/empty.zip&#039;|
|`BROKEN_ZIP`|public| |__DIR__ . &#039;/data/broken.zip&#039;|
|`MARKUP_XML_1`|public| |__DIR__ . &#039;/data/markup.1.xml&#039;|
|`MARKUP_XML_2`|public| |__DIR__ . &#039;/data/markup.2.xml&#039;|
|`MARKUP_XML_3`|public| |__DIR__ . &#039;/data/markup.3.xml&#039;|
|`MARKUP_XML_4`|public| |__DIR__ . &#039;/data/markup.4.xml&#039;|
|`MARKUP_XML_5`|public| |__DIR__ . &#039;/data/markup.5.xml&#039;|

## Properties


### epub



```php
protected \SebLucas\EPubMeta\EPub $epub
```






***

## Methods


### setUp



```php
protected setUp(): void
```












***

### tearDown



```php
protected tearDown(): void
```












***

### testGetZipEntries



```php
public testGetZipEntries(): void
```












***

### testLoadNonZip



```php
public testLoadNonZip(): void
```












***

### testLoadBrokenZip



```php
public testLoadBrokenZip(): void
```












***

### testLoadMissingFile



```php
public testLoadMissingFile(): void
```












***

### testLoadDirectory

We cannot expect a more specific exception message. ZipArchive::open returns 28
which is not known as an error code.

```php
public testLoadDirectory(): void
```












***

### testLoadEmptyZip



```php
public testLoadEmptyZip(): void
```












***

### testFilename



```php
public testFilename(): void
```












***

### testAuthors



```php
public testAuthors(): void
```












***

### testTitle



```php
public testTitle(): void
```












***

### testLanguage



```php
public testLanguage(): void
```












***

### testPublisher



```php
public testPublisher(): void
```












***

### testCopyright



```php
public testCopyright(): void
```












***

### testDescription



```php
public testDescription(): void
```












***

### testUniqueIdentifier



```php
public testUniqueIdentifier(): void
```












***

### testUuid



```php
public testUuid(): void
```












***

### testUri



```php
public testUri(): void
```












***

### testIsbn



```php
public testIsbn(): void
```












***

### testSubject



```php
public testSubject(): void
```












***

### testCover



```php
public testCover(): void
```












***

### testTitlePage



```php
public testTitlePage(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testCalibreAnnotations



```php
public testCalibreAnnotations(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testCalibreBookmarks



```php
public testCalibreBookmarks(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testManifest



```php
public testManifest(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testSpine



```php
public testSpine(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testToc



```php
public testToc(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testNav



```php
public testNav(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testNavTree



```php
public testNavTree(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testContents



```php
public testContents(string $referenceStart, string $referenceEnd, int $referenceSize, bool $keepMarkup, float $fraction): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$referenceStart` | **string** | The expected start of the extracted contents. |
| `$referenceEnd` | **string** | The expected end of the extracted contents. |
| `$referenceSize` | **int** | The expected size of the extracted contents. |
| `$keepMarkup` | **bool** | Whether to extract contents with or without HTML markup. |
| `$fraction` | **float** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### provideContentsTestParameters

Summary of provideContentsTestParameters

```php
public static provideContentsTestParameters(): array
```



* This method is **static**.








***

### testItemContents



```php
public testItemContents(string $referenceStart, string $referenceEnd, string $spineIndex, string $fragmentBegin = null, string $fragmentEnd = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$referenceStart` | **string** | The expected start of the extracted contents. |
| `$referenceEnd` | **string** | The expected end of the extracted contents. |
| `$spineIndex` | **string** | The spine index of the item to extract contents from. |
| `$fragmentBegin` | **string** | The anchor name (ID) where to start extraction. |
| `$fragmentEnd` | **string** | The anchor name (ID) where to end extraction. |




**Throws:**

- [`Exception`](./Exception.md)



***

### provideItemContentsTestParameters

Summary of provideItemContentsTestParameters

```php
public static provideItemContentsTestParameters(): array
```



* This method is **static**.








***

### testItemContentsStartFragmentException



```php
public testItemContentsStartFragmentException(): void
```












***

### testItemContentsEndFragmentException



```php
public testItemContentsEndFragmentException(): void
```












***

### testItemContentsMarkup



```php
public testItemContentsMarkup(string $referenceFile, string $spineIndex, string $fragmentBegin = null, string $fragmentEnd = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$referenceFile` | **string** |  |
| `$spineIndex` | **string** |  |
| `$fragmentBegin` | **string** |  |
| `$fragmentEnd` | **string** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### provideItemContentsMarkupTestParameters

Summary of provideItemContentsMarkupTestParameters

```php
public static provideItemContentsMarkupTestParameters(): array
```



* This method is **static**.








***

### testItemDataSize



```php
public testItemDataSize(): void
```











**Throws:**

- [`Exception`](./Exception.md)



***

### testZipEdit

Summary of testZipEdit

```php
public testZipEdit(): void
```












***


***
> Automatically generated on 2025-03-15
