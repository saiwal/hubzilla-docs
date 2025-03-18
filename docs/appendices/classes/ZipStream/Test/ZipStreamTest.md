
# ZipStreamTest





* Full name: `\ZipStream\Test\ZipStreamTest`
* Parent class: [`TestCase`](../../PHPUnit/Framework/TestCase.md)




## Methods


### testAddFile



```php
public testAddFile(): void
```












***

### testAddFileUtf8NameComment



```php
public testAddFileUtf8NameComment(): void
```












***

### testAddFileUtf8NameNonUtfComment



```php
public testAddFileUtf8NameNonUtfComment(): void
```












***

### testAddFileWithStorageMethod



```php
public testAddFileWithStorageMethod(): void
```












***

### testAddFileFromPath



```php
public testAddFileFromPath(): void
```












***

### testAddFileFromPathFileNotFoundException



```php
public testAddFileFromPathFileNotFoundException(): void
```












***

### testAddFileFromPathFileNotReadableException



```php
public testAddFileFromPathFileNotReadableException(): void
```












***

### testAddFileFromPathWithStorageMethod



```php
public testAddFileFromPathWithStorageMethod(): void
```












***

### testAddLargeFileFromPath



```php
public testAddLargeFileFromPath(): void
```












***

### testAddFileFromStream



```php
public testAddFileFromStream(): void
```












***

### testAddFileFromStreamUnreadableInput



```php
public testAddFileFromStreamUnreadableInput(): void
```












***

### testAddFileFromStreamBrokenOutputWrite



```php
public testAddFileFromStreamBrokenOutputWrite(): void
```












***

### testAddFileFromStreamBrokenInputRewind



```php
public testAddFileFromStreamBrokenInputRewind(): void
```












***

### testAddFileFromStreamUnseekableInputWithoutZeroHeader



```php
public testAddFileFromStreamUnseekableInputWithoutZeroHeader(): void
```












***

### testAddFileFromStreamUnseekableInputWithZeroHeader



```php
public testAddFileFromStreamUnseekableInputWithZeroHeader(): void
```












***

### testAddFileFromStreamWithStorageMethod



```php
public testAddFileFromStreamWithStorageMethod(): void
```












***

### testAddFileFromPsr7Stream



```php
public testAddFileFromPsr7Stream(): void
```












***

### testAddLargeFileFromPsr7Stream



```php
public testAddLargeFileFromPsr7Stream(): void
```












***

### testContinueFinishedZip



```php
public testContinueFinishedZip(): void
```












***

### testManyFilesWithoutZip64



```php
public testManyFilesWithoutZip64(): void
```












***

### testManyFilesWithZip64



```php
public testManyFilesWithZip64(): void
```












***

### testLongZipWithout64



```php
public testLongZipWithout64(): void
```












***

### testLongZipWith64



```php
public testLongZipWith64(): void
```












***

### testAddLargeFileWithoutZip64WithZeroHeader



```php
public testAddLargeFileWithoutZip64WithZeroHeader(): void
```












***

### testAddsZip64HeaderWhenNeeded



```php
public testAddsZip64HeaderWhenNeeded(): void
```












***

### testDoesNotAddZip64HeaderWhenNotNeeded



```php
public testDoesNotAddZip64HeaderWhenNotNeeded(): void
```












***

### testAddLargeFileWithoutZip64WithoutZeroHeader



```php
public testAddLargeFileWithoutZip64WithoutZeroHeader(): void
```












***

### testAddFileFromPsr7StreamWithOutputToPsr7Stream



```php
public testAddFileFromPsr7StreamWithOutputToPsr7Stream(): void
```












***

### testAddFileFromPsr7StreamWithFileSizeSet



```php
public testAddFileFromPsr7StreamWithFileSizeSet(): void
```












***

### testCreateArchiveHeaders



```php
public testCreateArchiveHeaders(): void
```












***

### testCreateArchiveWithFlushOptionSet



```php
public testCreateArchiveWithFlushOptionSet(): void
```












***

### testCreateArchiveWithOutputBufferingOffAndFlushOptionSet



```php
public testCreateArchiveWithOutputBufferingOffAndFlushOptionSet(): void
```












***

### testAddEmptyDirectory



```php
public testAddEmptyDirectory(): void
```












***

### testAddFileSimulate



```php
public testAddFileSimulate(): void
```












***

### testAddFileSimulateWithMaxSize



```php
public testAddFileSimulateWithMaxSize(): void
```












***

### testAddFileSimulateWithFstat



```php
public testAddFileSimulateWithFstat(): void
```












***

### testAddFileSimulateWithExactSizeZero



```php
public testAddFileSimulateWithExactSizeZero(): void
```












***

### testAddFileSimulateWithExactSizeInitial



```php
public testAddFileSimulateWithExactSizeInitial(): void
```












***

### testAddFileSimulateWithZeroSizeInFstat



```php
public testAddFileSimulateWithZeroSizeInFstat(): void
```












***

### testAddFileSimulateWithWrongExactSize



```php
public testAddFileSimulateWithWrongExactSize(): void
```












***

### testAddFileSimulateStrictZero



```php
public testAddFileSimulateStrictZero(): void
```












***

### testAddFileSimulateStrictInitial



```php
public testAddFileSimulateStrictInitial(): void
```












***

### testAddFileCallbackStrict



```php
public testAddFileCallbackStrict(): void
```












***

### testAddFileCallbackLax



```php
public testAddFileCallbackLax(): void
```












***

### testExecuteSimulation



```php
public testExecuteSimulation(): void
```












***

### testExecuteSimulationBeforeFinish



```php
public testExecuteSimulationBeforeFinish(): void
```












***

### addLargeFileFileFromPath



```php
private addLargeFileFileFromPath(\ZipStream\CompressionMethod $compressionMethod, mixed $zeroHeader, mixed $zip64): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compressionMethod` | **\ZipStream\CompressionMethod** |  |
| `$zeroHeader` | **mixed** |  |
| `$zip64` | **mixed** |  |





***


## Inherited methods


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

### getTmpFileStream



```php
protected getTmpFileStream(): array
```












***

### assertFileContains



```php
protected assertFileContains(string $filePath, string $needle): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filePath` | **string** |  |
| `$needle` | **string** |  |





***

### assertFileDoesNotContain



```php
protected assertFileDoesNotContain(string $filePath, string $needle): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filePath` | **string** |  |
| `$needle` | **string** |  |





***

### cmdExists



```php
protected cmdExists(string $command): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$command` | **string** |  |





***

### dumpZipContents



```php
protected dumpZipContents(string $path): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### validateAndExtractZip



```php
protected validateAndExtractZip(string $zipPath): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$zipPath` | **string** |  |





***

### zipArchiveOpenErrorCodeName



```php
protected zipArchiveOpenErrorCodeName(int $code): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **int** |  |





***

### getTmpDir



```php
protected getTmpDir(): string
```












***

### getRecursiveFileList



```php
protected getRecursiveFileList(string $path, bool $includeDirectories = false): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$includeDirectories` | **bool** |  |





***


***
> Automatically generated on 2025-03-18
