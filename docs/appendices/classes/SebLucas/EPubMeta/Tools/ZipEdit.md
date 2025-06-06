
# ZipEdit

ZipEdit class allows to edit zip files on the fly and stream them afterwards



* Full name: `\SebLucas\EPubMeta\Tools\ZipEdit`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DOWNLOAD`|public| |1|
|`NOHEADER`|public| |4|
|`FILE`|public| |8|
|`STRING`|public| |32|
|`MIME_TYPE`|public| |&#039;application/epub+zip&#039;|

## Properties


### mZip



```php
private \ZipArchive|null $mZip
```






***

### mEntries



```php
private array&lt;string,mixed&gt;|null $mEntries
```






***

### mChanges



```php
private array&lt;string,mixed&gt; $mChanges
```






***

### mFileName



```php
private string|null $mFileName
```






***

### mSaveMe



```php
private bool $mSaveMe
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### __destruct

Destructor

```php
public __destruct(): mixed
```












***

### Open

Open a zip file and read it's entries

```php
public Open(string $inFileName, int|null $inFlags): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** |  |
| `$inFlags` | **int&#124;null** |  |


**Return Value:**

True if zip file has been correctly opended, else false




***

### FileExists

Check if a file exist in the zip entries

```php
public FileExists(string $inFileName): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** | File to search |


**Return Value:**

True if the file exist, else false




***

### FileRead

Read the content of a file in the zip entries

```php
public FileRead(string $inFileName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** | File to search |


**Return Value:**

File content the file exist, else false




***

### FileStream

Get a file handler to a file in the zip entries (read-only)

```php
public FileStream(string $inFileName): resource|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** | File to search |


**Return Value:**

File handler if the file exist, else false




***

### FileAdd

Summary of FileAdd

```php
public FileAdd(string $inFileName, mixed $inData): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** |  |
| `$inData` | **mixed** |  |





***

### FileAddPath

Summary of FileAddPath

```php
public FileAddPath(string $inFileName, string $inFilePath): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** |  |
| `$inFilePath` | **string** |  |





***

### FileDelete

Summary of FileDelete

```php
public FileDelete(string $inFileName): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** |  |





***

### FileReplace

Replace the content of a file in the zip entries

```php
public FileReplace(string $inFileName, string|bool $inData): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** | File with content to replace |
| `$inData` | **string&#124;bool** | Data content to replace, or false to delete |





***

### FileGetState

Return the state of the file.

```php
public FileGetState(mixed $inFileName): string|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **mixed** |  |


**Return Value:**

'u'=unchanged, 'm'=modified, 'd'=deleted, 'a'=added, false=unknown




***

### FileCancelModif

Summary of FileCancelModif

```php
public FileCancelModif(string $inFileName, bool $ReplacedAndDeleted = true): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** |  |
| `$ReplacedAndDeleted` | **bool** |  |





***

### Close

Close the zip file

```php
public Close(): void
```











**Throws:**

- [`Exception`](../../../Exception.md)



***

### SaveBeforeClose

Summary of SaveBeforeClose

```php
public SaveBeforeClose(): void
```












***

### Flush

Summary of Flush

```php
public Flush(mixed $render = self::DOWNLOAD, mixed $outFileName = &#039;&#039;, mixed $contentType = &#039;&#039;, bool $sendHeaders = true, resource|null $outFileStream = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$render` | **mixed** |  |
| `$outFileName` | **mixed** |  |
| `$contentType` | **mixed** |  |
| `$sendHeaders` | **bool** |  |
| `$outFileStream` | **resource&#124;null** |  |





***

### copyTest

Summary of copyTest

```php
public static copyTest(string $inFileName, string $outFileName): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inFileName` | **string** |  |
| `$outFileName` | **string** |  |





***


***
> Automatically generated on 2025-03-18
