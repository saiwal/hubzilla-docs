***

# MonocleTest

Test for EPUB methods used by Monocle in COPS

Source: https://github.com/mikespub-org/seblucas

* Full name: `\MonocleTest`
* Parent class: [`TestCase`](./PHPUnit/Framework/TestCase.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TEST_EPUB`|public| |__DIR__ . &#039;/data/eng.epub&#039;|
|`TEST_EPUB_COPY`|public| |__DIR__ . &#039;/data/eng.copy.epub&#039;|
|`TEST_CONTENTS`|public| |__DIR__ . &#039;/data/eng.contents.json&#039;|
|`TEST_COMPONENTS`|public| |__DIR__ . &#039;/data/eng.components.json&#039;|
|`TEST_EPUB3`|public| |__DIR__ . &#039;/data/eng3.epub&#039;|

## Properties


### book



```php
private static \SebLucas\EPubMeta\EPub $book
```



* This property is **static**.


***

## Methods


### setUpBeforeClass



```php
public static setUpBeforeClass(): void
```



* This method is **static**.








***

### tearDownAfterClass



```php
public static tearDownAfterClass(): void
```



* This method is **static**.








***

### testComponents



```php
public testComponents(): void
```












***

### testContents



```php
public testContents(): void
```












***

### testComponent

Summary of testComponent

```php
public testComponent(string $component = &#039;text/titlepage.xhtml&#039;): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$component` | **string** |  |





***

### testGetComponentName

Summary of testGetComponentName

```php
public testGetComponentName(string $component = &#039;text/titlepage.xhtml&#039;, string $element = &#039;../images/cover.jpg&#039;): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$component` | **string** |  |
| `$element` | **string** |  |





***

### testComponentContentType

Summary of testComponentContentType

```php
public testComponentContentType(string $component = &#039;text/titlepage.xhtml&#039;): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$component` | **string** |  |





***

### testContentsEpub3



```php
public testContentsEpub3(): void
```












***

### encodeItem

Summary of encodeItem

```php
protected encodeItem(array $item, array $encoder): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **array** |  |
| `$encoder` | **array** |  |





***

### provideEncodeReplace

Summary of provideEncodeReplace

```php
public provideEncodeReplace(): array
```












***

### provideDecodeReplace

Summary of provideDecodeReplace

```php
public provideDecodeReplace(): array
```












***


***
> Automatically generated on 2025-03-15
