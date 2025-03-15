
# Item

An item of the EPUB manifest.



* Full name: `\SebLucas\EPubMeta\Data\Item`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`XHTML`|public| |&#039;application/xhtml+xml&#039;|

## Properties


### id



```php
protected string $id
```






***

### href



```php
protected string $href
```






***

### mediaType



```php
protected string $mediaType
```






***

### dataCallable



```php
protected callable|null $dataCallable
```






***

### data



```php
protected string $data
```






***

### size



```php
protected int $size
```






***

## Methods


### __construct



```php
public __construct(string $id, string $href, callable $dataCallable, int $size, string|null $mediaType = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | This Item’s identifier. |
| `$href` | **string** | The path to the corresponding file. |
| `$dataCallable` | **callable** | A callable to get data from the referenced file. |
| `$size` | **int** | The size of the referenced file. |
| `$mediaType` | **string&#124;null** | The media type of the corresponding file. If omitted XHTML is assumed. |





***

### getId



```php
public getId(): string
```












***

### getHref



```php
public getHref(): string
```












***

### getMediaType



```php
public getMediaType(): string
```












***

### getContents

Extract (a part of) the contents from the referenced XML file.

```php
public getContents(string|null $fragmentBegin = null, string|null $fragmentEnd = null, bool $keepMarkup = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fragmentBegin` | **string&#124;null** | ID of the element where to start reading the contents. |
| `$fragmentEnd` | **string&#124;null** | ID of the element where to stop reading the contents. |
| `$keepMarkup` | **bool** | Whether to keep the XHTML markup rather than extracted plain text. |


**Return Value:**

The contents of that fragment.



**Throws:**

- [`Exception`](../../../Exception.md)



***

### getData

Get the file data.

```php
public getData(): string
```









**Return Value:**

The binary data of the corresponding file.




***

### getSize

Get the size of the corresponding file.

```php
public getSize(): int
```












***


***
> Automatically generated on 2025-03-15
