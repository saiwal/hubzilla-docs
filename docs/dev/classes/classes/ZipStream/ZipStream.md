
# ZipStream

Streamed, dynamically generated zip archives.

## Usage

Streaming zip archives is a simple, three-step process:

1.  Create the zip stream:

```php
$zip = new ZipStream(outputName: 'example.zip');
```

2.  Add one or more files to the archive:

```php
// add first file
$zip->addFile(fileName: 'world.txt', data: 'Hello World');

// add second file
$zip->addFile(fileName: 'moon.txt', data: 'Hello Moon');
```

3.  Finish the zip stream:

```php
$zip->finish();
```

You can also add an archive comment, add comments to individual files,
and adjust the timestamp of files. See the API documentation for each
method below for additional information.

## Example

```php
// create a new zip stream object
$zip = new ZipStream(outputName: 'some_files.zip');

// list of local files
$files = array('foo.txt', 'bar.jpg');

// read and add each file to the archive
foreach ($files as $path)
  $zip->addFileFromPath(fileName: $path, $path);

// write archive footer to stream
$zip->finish();
```

* Full name: `\ZipStream\ZipStream`



## Properties


### ready



```php
private bool $ready
```






***

### offset



```php
private int $offset
```






***

### centralDirectoryRecords



```php
private string[] $centralDirectoryRecords
```






***

### outputStream



```php
private resource $outputStream
```






***

### httpHeaderCallback



```php
private \Closure $httpHeaderCallback
```






***

### recordedSimulation



```php
private \ZipStream\File[] $recordedSimulation
```






***

### operationMode



```php
private \ZipStream\OperationMode $operationMode
```






***

### comment



```php
private string $comment
```






***

### defaultCompressionMethod



```php
private \ZipStream\CompressionMethod $defaultCompressionMethod
```






***

### defaultDeflateLevel



```php
private int $defaultDeflateLevel
```






***

### enableZip64



```php
private bool $enableZip64
```






***

### defaultEnableZeroHeader



```php
private bool $defaultEnableZeroHeader
```






***

### sendHttpHeaders



```php
private bool $sendHttpHeaders
```






***

### outputName



```php
private ?string $outputName
```






***

### contentDisposition



```php
private string $contentDisposition
```






***

### contentType



```php
private string $contentType
```






***

### flushOutput



```php
private bool $flushOutput
```






***

## Methods


### __construct

Create a new ZipStream object.

```php
public __construct(\ZipStream\OperationMode $operationMode = OperationMode::NORMAL, string $comment = &#039;&#039;, \Psr\Http\Message\StreamInterface|resource|null $outputStream = null, \ZipStream\CompressionMethod $defaultCompressionMethod = CompressionMethod::DEFLATE, int $defaultDeflateLevel = 6, bool $enableZip64 = true, bool $defaultEnableZeroHeader = true, bool $sendHttpHeaders = true, ?\Closure $httpHeaderCallback = null, string|null $outputName = null, string $contentDisposition = &#039;attachment&#039;, string $contentType = &#039;application/x-zip&#039;, bool $flushOutput = false): self
```

##### Examples

```php
// create a new zip file named 'foo.zip'
$zip = new ZipStream(outputName: 'foo.zip');

// create a new zip file named 'bar.zip' with a comment
$zip = new ZipStream(
  outputName: 'bar.zip',
  comment: 'this is a comment for the zip file.',
);
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$operationMode` | **\ZipStream\OperationMode** | <br />The mode can be used to switch between `NORMAL` and `SIMULATION_*` modes.<br />For details see the `OperationMode` documentation.<br /><br />Default to `NORMAL`. |
| `$comment` | **string** | <br />Archive Level Comment |
| `$outputStream` | **\Psr\Http\Message\StreamInterface&#124;resource&#124;null** | <br />Override the output of the archive to a different target.<br /><br />By default the archive is sent to `STDOUT`. |
| `$defaultCompressionMethod` | **\ZipStream\CompressionMethod** | <br />How to handle file compression. Legal values are<br />`CompressionMethod::DEFLATE` (the default), or<br />`CompressionMethod::STORE`. `STORE` sends the file raw and is<br />significantly faster, while `DEFLATE` compresses the file and<br />is much, much slower. |
| `$defaultDeflateLevel` | **int** | <br />Default deflation level. Only relevant if `compressionMethod`<br />is `DEFLATE`.<br /><br />See details of [`deflate_init`](https://www.php.net/manual/en/function.deflate-init.php#refsect1-function.deflate-init-parameters) |
| `$enableZip64` | **bool** | <br />Enable Zip64 extension, supporting very large<br />archives (any size &gt; 4 GB or file count &gt; 64k) |
| `$defaultEnableZeroHeader` | **bool** | <br />Enable streaming files with single read.<br /><br />When the zero header is set, the file is streamed into the output<br />and the size &amp; checksum are added at the end of the file. This is the<br />fastest method and uses the least memory. Unfortunately not all<br />ZIP clients fully support this and can lead to clients reporting<br />the generated ZIP files as corrupted in combination with other<br />circumstances. (Zip64 enabled, using UTF8 in comments / names etc.)<br /><br />When the zero header is not set, the length &amp; checksum need to be<br />defined before the file is actually added. To prevent loading all<br />the data into memory, the data has to be read twice. If the data<br />which is added is not seekable, this call will fail. |
| `$sendHttpHeaders` | **bool** | <br />Boolean indicating whether or not to send<br />the HTTP headers for this file. |
| `$httpHeaderCallback` | **?\Closure** | <br />The method called to send HTTP headers |
| `$outputName` | **string&#124;null** | <br />The name of the created archive.<br /><br />Only relevant if `$sendHttpHeaders = true`. |
| `$contentDisposition` | **string** | <br />HTTP Content-Disposition<br /><br />Only relevant if `sendHttpHeaders = true`. |
| `$contentType` | **string** | <br />HTTP Content Type<br /><br />Only relevant if `sendHttpHeaders = true`. |
| `$flushOutput` | **bool** | <br />Enable flush after every write to output stream. |





***

### addFile

Add a file to the archive.

```php
public addFile(string $fileName, string $data, string $comment = &#039;&#039;, ?\ZipStream\CompressionMethod $compressionMethod = null, ?int $deflateLevel = null, ?\DateTimeInterface $lastModificationDateTime = null, ?int $maxSize = null, ?int $exactSize = null, ?bool $enableZeroHeader = null): void
```

##### File Options

See {@see \ZipStream\addFileFromPsr7Stream()}

##### Examples

```php
// add a file named 'world.txt'
$zip->addFile(fileName: 'world.txt', data: 'Hello World!');

// add a file named 'bar.jpg' with a comment and a last-modified
// time of two hours ago
$zip->addFile(
  fileName: 'bar.jpg',
  data: $data,
  comment: 'this is a comment about bar.jpg',
  lastModificationDateTime: new DateTime('2 hours ago'),
);
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fileName` | **string** |  |
| `$data` | **string** | <br /><br />contents of file |
| `$comment` | **string** |  |
| `$compressionMethod` | **?\ZipStream\CompressionMethod** |  |
| `$deflateLevel` | **?int** |  |
| `$lastModificationDateTime` | **?\DateTimeInterface** |  |
| `$maxSize` | **?int** |  |
| `$exactSize` | **?int** |  |
| `$enableZeroHeader` | **?bool** |  |





***

### addFileFromPath

Add a file at path to the archive.

```php
public addFileFromPath(string $fileName, string $path, string $comment = &#039;&#039;, ?\ZipStream\CompressionMethod $compressionMethod = null, ?int $deflateLevel = null, ?\DateTimeInterface $lastModificationDateTime = null, ?int $maxSize = null, ?int $exactSize = null, ?bool $enableZeroHeader = null): void
```

##### File Options

See {@see \ZipStream\addFileFromPsr7Stream()}

###### Examples

```php
// add a file named 'foo.txt' from the local file '/tmp/foo.txt'
$zip->addFileFromPath(
  fileName: 'foo.txt',
  path: '/tmp/foo.txt',
);

// add a file named 'bigfile.rar' from the local file
// '/usr/share/bigfile.rar' with a comment and a last-modified
// time of two hours ago
$zip->addFileFromPath(
  fileName: 'bigfile.rar',
  path: '/usr/share/bigfile.rar',
  comment: 'this is a comment about bigfile.rar',
  lastModificationDateTime: new DateTime('2 hours ago'),
);
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fileName` | **string** |  |
| `$path` | **string** |  |
| `$comment` | **string** |  |
| `$compressionMethod` | **?\ZipStream\CompressionMethod** |  |
| `$deflateLevel` | **?int** |  |
| `$lastModificationDateTime` | **?\DateTimeInterface** |  |
| `$maxSize` | **?int** |  |
| `$exactSize` | **?int** |  |
| `$enableZeroHeader` | **?bool** |  |




**Throws:**

- [`FileNotFoundException`](./Exception/FileNotFoundException.md)

- [`FileNotReadableException`](./Exception/FileNotReadableException.md)



***

### addFileFromStream

Add an open stream (resource) to the archive.

```php
public addFileFromStream(string $fileName, resource $stream, string $comment = &#039;&#039;, ?\ZipStream\CompressionMethod $compressionMethod = null, ?int $deflateLevel = null, ?\DateTimeInterface $lastModificationDateTime = null, ?int $maxSize = null, ?int $exactSize = null, ?bool $enableZeroHeader = null): void
```

##### File Options

See {@see \ZipStream\addFileFromPsr7Stream()}

##### Examples

```php
// create a temporary file stream and write text to it
$filePointer = tmpfile();
fwrite($filePointer, 'The quick brown fox jumped over the lazy dog.');

// add a file named 'streamfile.txt' from the content of the stream
$archive->addFileFromStream(
  fileName: 'streamfile.txt',
  stream: $filePointer,
);
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fileName` | **string** |  |
| `$stream` | **resource** | contents of file as a stream resource |
| `$comment` | **string** |  |
| `$compressionMethod` | **?\ZipStream\CompressionMethod** |  |
| `$deflateLevel` | **?int** |  |
| `$lastModificationDateTime` | **?\DateTimeInterface** |  |
| `$maxSize` | **?int** |  |
| `$exactSize` | **?int** |  |
| `$enableZeroHeader` | **?bool** |  |





***

### addFileFromPsr7Stream

Add an open stream to the archive.

```php
public addFileFromPsr7Stream(string $fileName, \Psr\Http\Message\StreamInterface $stream, string $comment = &#039;&#039;, ?\ZipStream\CompressionMethod $compressionMethod = null, ?int $deflateLevel = null, ?\DateTimeInterface $lastModificationDateTime = null, ?int $maxSize = null, ?int $exactSize = null, ?bool $enableZeroHeader = null): void
```

##### Examples

```php
$stream = $response->getBody();
// add a file named 'streamfile.txt' from the content of the stream
$archive->addFileFromPsr7Stream(
  fileName: 'streamfile.txt',
  stream: $stream,
);
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fileName` | **string** | <br />path of file in archive (including directory) |
| `$stream` | **\Psr\Http\Message\StreamInterface** | <br />contents of file as a stream resource |
| `$comment` | **string** | <br />ZIP comment for this file |
| `$compressionMethod` | **?\ZipStream\CompressionMethod** | <br />Override `defaultCompressionMethod`<br /><br />See {@see \ZipStream\__construct()} |
| `$deflateLevel` | **?int** | <br />Override `defaultDeflateLevel`<br /><br />See {@see \ZipStream\__construct()} |
| `$lastModificationDateTime` | **?\DateTimeInterface** | <br />Set last modification time of file.<br /><br />Default: `now` |
| `$maxSize` | **?int** | <br />Only read `maxSize` bytes from file.<br /><br />The file is considered done when either reaching `EOF`<br />or the `maxSize`. |
| `$exactSize` | **?int** | <br />Read exactly `exactSize` bytes from file.<br />If `EOF` is reached before reading `exactSize` bytes, an error will be<br />thrown. The parameter allows for faster size calculations if the `stream`<br />does not support `fstat` size or is slow and otherwise known beforehand. |
| `$enableZeroHeader` | **?bool** | <br />Override `defaultEnableZeroHeader`<br /><br />See {@see \ZipStream\__construct()} |





***

### addFileFromCallback

Add a file based on a callback.

```php
public addFileFromCallback(string $fileName, \Closure $callback, string $comment = &#039;&#039;, ?\ZipStream\CompressionMethod $compressionMethod = null, ?int $deflateLevel = null, ?\DateTimeInterface $lastModificationDateTime = null, ?int $maxSize = null, ?int $exactSize = null, ?bool $enableZeroHeader = null): void
```

This is useful when you want to simulate a lot of files without keeping
all of the file handles open at the same time.

##### Examples

```php
foreach($files as $name => $size) {
  $archive->addFileFromCallback(
    fileName: 'streamfile.txt',
    exactSize: $size,
    callback: function() use($name): Psr\Http\Message\StreamInterface {
      $response = download($name);
      return $response->getBody();
    }
  );
}
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fileName` | **string** | <br />path of file in archive (including directory) |
| `$callback` | **\Closure** |  |
| `$comment` | **string** | <br />ZIP comment for this file |
| `$compressionMethod` | **?\ZipStream\CompressionMethod** | <br />Override `defaultCompressionMethod`<br /><br />See {@see \ZipStream\__construct()} |
| `$deflateLevel` | **?int** | <br />Override `defaultDeflateLevel`<br /><br />See {@see \ZipStream\__construct()} |
| `$lastModificationDateTime` | **?\DateTimeInterface** | <br />Set last modification time of file.<br /><br />Default: `now` |
| `$maxSize` | **?int** | <br />Only read `maxSize` bytes from file.<br /><br />The file is considered done when either reaching `EOF`<br />or the `maxSize`. |
| `$exactSize` | **?int** | <br />Read exactly `exactSize` bytes from file.<br />If `EOF` is reached before reading `exactSize` bytes, an error will be<br />thrown. The parameter allows for faster size calculations if the `stream`<br />does not support `fstat` size or is slow and otherwise known beforehand. |
| `$enableZeroHeader` | **?bool** | <br />Override `defaultEnableZeroHeader`<br /><br />See {@see \ZipStream\__construct()} |





***

### addDirectory

Add a directory to the archive.

```php
public addDirectory(string $fileName, string $comment = &#039;&#039;, ?\DateTimeInterface $lastModificationDateTime = null): void
```

##### File Options

See {@see \ZipStream\addFileFromPsr7Stream()}

##### Examples

```php
// add a directory named 'world/'
$zip->addDirectory(fileName: 'world/');
```






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fileName` | **string** |  |
| `$comment` | **string** |  |
| `$lastModificationDateTime` | **?\DateTimeInterface** |  |





***

### executeSimulation

Executes a previously calculated simulation.

```php
public executeSimulation(): void
```

##### Example

```php
$zip = new ZipStream(
  outputName: 'foo.zip',
  operationMode: OperationMode::SIMULATE_STRICT,
);

$zip->addFile('test.txt', 'Hello World');

$size = $zip->finish();

header('Content-Length: '. $size);

$zip->executeSimulation();
```










***

### finish

Write zip footer to stream.

```php
public finish(): int
```

The clase is left in an unusable state after `finish`.

##### Example

```php
// write footer to stream
$zip->finish();
```










***

### normalizeStream



```php
private static normalizeStream(\Psr\Http\Message\StreamInterface|resource|null $outputStream): resource
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$outputStream` | **\Psr\Http\Message\StreamInterface&#124;resource&#124;null** |  |





***

### recordSentBytes

Record sent bytes

```php
private recordSentBytes(int $sentBytes): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sentBytes` | **int** |  |





***

### send

Send string, sending HTTP headers if necessary.

```php
private send(string $data): void
```

Flush output after write if configure option is set.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### sendHttpHeaders

Send HTTP headers for this stream.

```php
private sendHttpHeaders(): void
```












***

### clear

Clear all internal variables. Note that the stream object is not
usable after this.

```php
private clear(): void
```












***


***
> Automatically generated on 2025-03-15
