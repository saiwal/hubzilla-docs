
# Other





* Full name: `\SebLucas\EPubMeta\Other`
* Parent class: [`\SebLucas\EPubMeta\EPub`](./EPub.md)




## Methods


### setMeta

A simple setter for simple meta attributes

```php
protected setMeta(string $item, string $value, bool|string $attribute = false, bool|string $attributeValue = false, bool $caseSensitive = true): mixed
```

It should only be used for attributes that are expected to be unique






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string** | XML node to set |
| `$value` | **string** | New node value |
| `$attribute` | **bool&#124;string** | Attribute name |
| `$attributeValue` | **bool&#124;string** | Attribute value |
| `$caseSensitive` | **bool** |  |





***

### getMeta

A simple getter for simple meta attributes

```php
protected getMeta(string $item, bool|string $att = false, bool|string $aval = false, bool $caseSensitive = true): string
```

It should only be used for attributes that are expected to be unique






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string** | XML node to get |
| `$att` | **bool&#124;string** | Attribute name |
| `$aval` | **bool&#124;string** | Attribute value |
| `$caseSensitive` | **bool** |  |





***

### sync

Sync XPath object with updated DOM.

```php
protected sync(): mixed
```












***


## Inherited methods


### __construct

Constructor

```php
public __construct(string $file, string $zipClass = ZipFile::class): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** | path to epub file to work on |
| `$zipClass` | **string** | class to handle zip - ZipFile is read-only |




**Throws:**
<p>if metadata could not be loaded</p>

- [`Exception`](../../Exception.md)



***

### openZipFile

Summary of openZipFile

```php
public openZipFile(string $zipClass): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$zipClass` | **string** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### loadMetadata

Summary of loadMetadata

```php
public loadMetadata(): void
```











**Throws:**

- [`Exception`](../../Exception.md)



***

### loadXmlData

Summary of loadXmlData

```php
public loadXmlData(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### initSpineComponent

Summary of initSpineComponent

```php
public initSpineComponent(): void
```











**Throws:**

- [`Exception`](../../Exception.md)



***

### loadNavData

Summary of loadNavData

```php
public loadNavData(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### loadTocData

Summary of loadTocData

```php
public loadTocData(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### getEpubVersion

Get the ePub version

```php
public getEpubVersion(): int
```









**Return Value:**

The number of the ePub version (2 or 3 for now) or 0 if not found




***

### file

file name getter

```php
public file(): string
```












***

### meta

meta file getter

```php
public meta(): string
```












***

### close

Close the epub file

```php
public close(): void
```












***

### cleanITunesCrap

Remove iTunes files

```php
public cleanITunesCrap(): void
```












***

### save

Writes back all meta data changes

```php
public save(): void
```












***

### download

Get the updated epub

```php
public download(mixed $file = false, bool $sendHeaders = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |
| `$sendHeaders` | **bool** |  |





***

### components

Get the components list as an array

```php
public components(): array
```












***

### component

Get the component content

```php
public component(mixed $comp): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$comp` | **mixed** |  |





***

### getComponentName

Summary of getComponentName

```php
public getComponentName(mixed $comp, mixed $elementPath): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$comp` | **mixed** |  |
| `$elementPath` | **mixed** |  |





***

### encodeComponentName

Encode the component name (to replace / and -)

```php
protected static encodeComponentName(mixed $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **mixed** |  |





***

### decodeComponentName

Decode the component name (to replace / and -)

```php
protected static decodeComponentName(mixed $src): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$src` | **mixed** |  |





***

### componentContentType

Get the component content type

```php
public componentContentType(mixed $comp): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$comp` | **mixed** |  |





***

### getComponentSize

Summary of getComponentSize

```php
public getComponentSize(mixed $comp): bool|int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$comp` | **mixed** |  |





***

### getNavPointDetail

EPUB 2 navigation control file (NCX format)
See https://idpf.org/epub/20/spec/OPF_2.0_latest.htm#Section2.4.1

```php
protected getNavPointDetail(mixed $node): array&lt;string,string&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **mixed** |  |





***

### getNavTocListItem

EPUB 3 navigation document (toc nav element)
See https://www.w3.org/TR/epub-33/#sec-nav-toc

```php
protected getNavTocListItem(mixed $node): array&lt;string,string&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **mixed** |  |





***

### contents

Get the Epub content (TOC) as an array

```php
public contents(): mixed
```

For each chapter there is a "title" and a "src", and optional "children"
See https://github.com/joseph/Monocle/wiki/Book-data-object for details










***

### setAuthors

Set the book author(s)

```php
public setAuthors(mixed $authors): void
```

Authors should be given with a "file-as" and a real name. The file as
is used for sorting in e-readers.

Example:

array(
     'Pratchett, Terry'   => 'Terry Pratchett',
     'Simpson, Jacqueline' => 'Jacqueline Simpson',
)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$authors` | **mixed** |  |





***

### getAuthors

Get the book author(s)

```php
public getAuthors(): string[]
```












***

### Google

Set or get the Google Books ID

```php
public Google(string|bool $google = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$google` | **string&#124;bool** |  |





***

### Amazon

Set or get the Amazon ID of the book

```php
public Amazon(string|bool $amazon = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$amazon` | **string&#124;bool** |  |





***

### setSeries

Set the Series of the book

```php
public setSeries(string $serie): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$serie` | **string** |  |





***

### getSeries

Get the Series of the book

```php
public getSeries(): mixed
```












***

### setSeriesIndex

Set the Series Index of the book

```php
public setSeriesIndex(string $seriesIndex): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$seriesIndex` | **string** |  |





***

### getSeriesIndex

Get the Series Index of the book

```php
public getSeriesIndex(): mixed
```












***

### setSubjects

Set the book's subjects (aka. tags)

```php
public setSubjects(string[]|string $subjects): void
```

Subject should be given as array, but a comma separated string will also
be accepted.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subjects` | **string[]&#124;string** |  |





***

### getSubjects

Get the book's subjects (aka. tags)

```php
public getSubjects(): array
```












***

### setCoverInfo

Update the cover data

```php
public setCoverInfo(string $path, string $mime): void
```

When adding a new image this function return no or old data because the
image contents are not in the epub file, yet. The image will be added when
the save() method is called.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** | local filesystem path to a new cover image |
| `$mime` | **string** | mime type of the given file |





***

### getCoverInfo

Read the cover data

```php
public getCoverInfo(): array
```

Returns an associative array with the following keys:

  mime  - filetype (usually image/jpeg)
  data  - the binary image data
  found - the internal path, or false if no image is set in epub

When no image is set in the epub file, the binary data for a transparent
GIF pixel is returned.










***

### getCoverId

Summary of getCoverId

```php
public getCoverId(): string|null
```












***

### getCoverItem

Summary of getCoverItem

```php
public getCoverItem(): \SebLucas\EPubMeta\Dom\Element|null
```












***

### getCoverPath

Get the internal path of the cover image file.

```php
public getCoverPath(): string|null
```












***

### Combine

Summary of Combine

```php
public static Combine(mixed $a, mixed $b): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **mixed** |  |
| `$b` | **mixed** |  |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### getFullPath

Summary of getFullPath

```php
protected getFullPath(mixed $file, mixed $context = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |
| `$context` | **mixed** |  |





***

### updateForKepub

Summary of updateForKepub

```php
public updateForKepub(): void
```












***

### setCoverFile

Summary of setCoverFile

```php
public setCoverFile(string $path, string $mime): array|void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$mime` | **string** |  |





***

### getAttr

Summary of getAttr

```php
protected static getAttr(\DOMNodeList&lt;\SebLucas\EPubMeta\Dom\Element&gt; $nodes, string $att): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$nodes` | **\DOMNodeList<\SebLucas\EPubMeta\Dom\Element>** | list of Element items |
| `$att` | **string** | Attribute name |





***

### deleteNodes

Summary of deleteNodes

```php
protected static deleteNodes(\DOMNodeList&lt;\SebLucas\EPubMeta\Dom\Element&gt; $nodes): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$nodes` | **\DOMNodeList<\SebLucas\EPubMeta\Dom\Element>** | list of Element items |





***

### getset

A simple getter/setter for simple meta attributes

```php
protected getset(string $item, string|bool $value = false, string|bool $att = false, string|bool|array $aval = false, string|bool $datt = false): string|void
```

It should only be used for attributes that are expected to be unique






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string** | XML node to set/get |
| `$value` | **string&#124;bool** | New node value |
| `$att` | **string&#124;bool** | Attribute name |
| `$aval` | **string&#124;bool&#124;array** | Attribute value |
| `$datt` | **string&#124;bool** | Destination attribute |





***

### no_cover

Return a not found response for Cover()

```php
protected no_cover(): array&lt;string,mixed&gt;
```












***

### reparse

Reparse the DOM tree

```php
protected reparse(): void
```

I had to rely on this because otherwise xpath failed to find the newly
added nodes










***

### setMeta

A simple setter for simple meta attributes

```php
protected setMeta(string $item, string $value, bool|string $attribute = false, bool|string $attributeValue = false, bool $caseSensitive = true): mixed
```

It should only be used for attributes that are expected to be unique






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string** | XML node to set |
| `$value` | **string** | New node value |
| `$attribute` | **bool&#124;string** | Attribute name |
| `$attributeValue` | **bool&#124;string** | Attribute value |
| `$caseSensitive` | **bool** |  |





***

### getMeta

A simple getter for simple meta attributes

```php
protected getMeta(string $item, bool|string $att = false, bool|string $aval = false, bool $caseSensitive = true): string
```

It should only be used for attributes that are expected to be unique






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string** | XML node to get |
| `$att` | **bool&#124;string** | Attribute name |
| `$aval` | **bool&#124;string** | Attribute value |
| `$caseSensitive` | **bool** |  |





***

### setMetaDestination

A simple setter for simple meta attributes - with destination attribute (for Serie)

```php
protected setMetaDestination(string $item, string $attribute, string $attributeValue, string $datt, string $value): mixed
```

It should only be used for attributes that are expected to be unique






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string** | XML node to set |
| `$attribute` | **string** | Attribute name |
| `$attributeValue` | **string** | Attribute value |
| `$datt` | **string** | Destination attribute |
| `$value` | **string** | New node value |





***

### getMetaDestination

A simple getter for simple meta attributes - with destination attribute (for Serie)

```php
protected getMetaDestination(string $item, string $att, string $aval, string $datt): string
```

It should only be used for attributes that are expected to be unique






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string** | XML node to get |
| `$att` | **string** | Attribute name |
| `$aval` | **string** | Attribute value |
| `$datt` | **string** | Destination attribute |





***

### setTitle

Set the book title

```php
public setTitle(string $title): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$title` | **string** |  |





***

### getTitle

Get the book title

```php
public getTitle(): mixed
```












***

### setLanguage

Set the book's language

```php
public setLanguage(string $lang): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang` | **string** |  |





***

### getLanguage

Get the book's language

```php
public getLanguage(): mixed
```












***

### setPublisher

Set the book's publisher info

```php
public setPublisher(string $publisher): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$publisher` | **string** |  |





***

### getPublisher

Get the book's publisher info

```php
public getPublisher(): string
```












***

### setCopyright

Set the book's copyright info

```php
public setCopyright(string $rights): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rights` | **string** |  |





***

### getCopyright

Get the book's copyright info

```php
public getCopyright(): string
```












***

### setDescription

Set the book's description

```php
public setDescription(string $description): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$description` | **string** |  |





***

### getDescription

Get the book's description

```php
public getDescription(): string
```












***

### setEventDate

Set a date for an event in the package file’s meta section.

```php
public setEventDate(string $event, string $date): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$event` | **string** |  |
| `$date` | **string** | Date eg: 2012-05-19T12:54:25Z |





***

### getEventDate

Get a date for an event in the package file’s meta section.

```php
public getEventDate(string $event): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$event` | **string** |  |





***

### setCreationDate

Set the book's creation date

```php
public setCreationDate(string $date): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** | Date eg: 2012-05-19T12:54:25Z |





***

### getCreationDate

Get the book's creation date

```php
public getCreationDate(): mixed
```












***

### setModificationDate

Set the book's modification date

```php
public setModificationDate(string $date): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date` | **string** | Date eg: 2012-05-19T12:54:25Z |





***

### getModificationDate

Get the book's modification date

```php
public getModificationDate(): mixed
```












***

### setIdentifier

Set an identifier in the package file’s meta section.

```php
public setIdentifier(string|string[] $idScheme, string $value, bool $caseSensitive = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$idScheme` | **string&#124;string[]** | The identifier’s scheme. If an array is given<br />all matching identifiers are replaced by one with the first value as scheme. |
| `$value` | **string** |  |
| `$caseSensitive` | **bool** |  |





***

### getIdentifier

Set an identifier from the package file’s meta section.

```php
public getIdentifier(string|string[] $idScheme, bool $caseSensitive = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$idScheme` | **string&#124;string[]** | The identifier’s scheme. If an array is given<br />the scheme can be any of its values. |
| `$caseSensitive` | **bool** | - @todo changed to true here |


**Return Value:**

The value of the first matching element.




***

### setUniqueIdentifier

Set the book's unique identifier

```php
public setUniqueIdentifier(string $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





***

### getUniqueIdentifier

Get the book's unique identifier

```php
public getUniqueIdentifier(bool $normalize = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$normalize` | **bool** |  |





***

### setUuid

Set the book's UUID - @todo pick one + case sensitive

```php
public setUuid(string $uuid): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **string** |  |





***

### getUuid

Get the book's UUID - @todo pick one + case sensitive

```php
public getUuid(): string
```












***

### setUri

Set the book's URI

```php
public setUri(string $uri): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getUri

Get the book's URI

```php
public getUri(): string
```












***

### setIsbn

Set the book's ISBN

```php
public setIsbn(string $isbn): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$isbn` | **string** |  |





***

### getIsbn

Get the book's ISBN

```php
public getIsbn(): string
```












***

### setCalibre

Set the Calibre UUID of the book

```php
public setCalibre(string $uuid): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **string** |  |





***

### getCalibre

Get the Calibre UUID of the book

```php
public getCalibre(): string
```












***

### clearCover

Remove the cover image

```php
public clearCover(): void
```

If the actual image file was added by this library it will be removed. Otherwise only the
reference to it is removed from the metadata, since the same image might be referenced
by other parts of the EPUB file.










***

### setCover

Set the cover image

```php
public setCover(string $path, string $mime): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** | local filesystem path to a new cover image |
| `$mime` | **string** | mime type of the given file |





***

### getCover

Get the cover image

```php
public getCover(): string|null
```









**Return Value:**

The binary image data or null if no image exists.




***

### hasCover

Whether a cover image meta entry does exist.

```php
public hasCover(): bool
```












***

### addCoverImageTitlePage

Add a title page with the cover image to the EPUB.

```php
public addCoverImageTitlePage(string $templatePath = __DIR__ . &#039;/../templates/titlepage.xhtml&#039;): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$templatePath` | **string** | The path to the template file. Defaults to an XHTML file contained in this library. |





***

### removeTitlePage

Remove the title page added by this library (determined by a certain manifest item ID).

```php
public removeTitlePage(): void
```












***

### getCalibreAnnotations

Get the Calibre book annotations from opf:metadata (if saved)

```php
public getCalibreAnnotations(?string $data = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **?string** |  |





***

### getCalibreBookmarks

Get the Calibre bookmarks from META-INF/calibre_bookmarks.txt (if saved)

```php
public getCalibreBookmarks(?string $data = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **?string** |  |





***

### getManifest

Get the manifest of this EPUB.

```php
public getManifest(): \SebLucas\EPubMeta\Data\Manifest
```











**Throws:**

- [`Exception`](../../Exception.md)



***

### getSpine

Get the spine structure of this EPUB.

```php
public getSpine(): \SebLucas\EPubMeta\Contents\Spine
```











**Throws:**

- [`Exception`](../../Exception.md)



***

### getToc

Get the table of contents structure of this EPUB.

```php
public getToc(): \SebLucas\EPubMeta\Contents\Toc|\SebLucas\EPubMeta\Contents\Nav
```











**Throws:**

- [`Exception`](../../Exception.md)



***

### loadNavPoints

Load navigation points from TOC XML DOM into TOC object structure.

```php
protected static loadNavPoints(\DOMNodeList&lt;\SebLucas\EPubMeta\EPubDomElement&gt; $navPointNodes, \SebLucas\EPubMeta\Contents\NavPointList $navPointList, \SebLucas\EPubMeta\Dom\XPath $xp): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$navPointNodes` | **\DOMNodeList<\SebLucas\EPubMeta\EPubDomElement>** | List of nodes to load from. |
| `$navPointList` | **\SebLucas\EPubMeta\Contents\NavPointList** | List structure to load into. |
| `$xp` | **\SebLucas\EPubMeta\Dom\XPath** | The XPath of the TOC document. |





***

### getNav

Summary of getNav

```php
public getNav(): \SebLucas\EPubMeta\Contents\Toc|\SebLucas\EPubMeta\Contents\Nav
```












***

### loadNavList

Load navigation points from NAV XML DOM into NAV object structure.

```php
protected static loadNavList(\DOMNodeList&lt;\SebLucas\EPubMeta\EPubDomElement&gt; $navListNodes, \SebLucas\EPubMeta\Contents\NavPointList $navPointList, \SebLucas\EPubMeta\Dom\XPath $xp, int $depth, int $order): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$navListNodes` | **\DOMNodeList<\SebLucas\EPubMeta\EPubDomElement>** | List of nodes to load from. |
| `$navPointList` | **\SebLucas\EPubMeta\Contents\NavPointList** | List structure to load into. |
| `$xp` | **\SebLucas\EPubMeta\Dom\XPath** | The XPath of the NAV document. |
| `$depth` | **int** | Current depth of this list (recursive) |
| `$order` | **int** | Current start order for this list |





***

### getContents

Extract the contents of this EPUB.

```php
public getContents(bool $keepMarkup = false, float $fraction = 1.0): string
```

This concatenates contents of items according to their order in the spine.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$keepMarkup` | **bool** | Whether to keep the XHTML markup rather than extracted plain text. |
| `$fraction` | **float** | If less than 1, only the respective part from the beginning of the book is extracted. |


**Return Value:**

The contents of this EPUB.



**Throws:**

- [`Exception`](../../Exception.md)



***

### buildMetaXPath

Build an XPath expression to select certain nodes in the metadata section.

```php
protected static buildMetaXPath(string $element, string $attribute, string|string[] $value, bool $caseSensitive = true): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **string** | The node name of the elements to select. |
| `$attribute` | **string** | If set, the attribute required in the element. |
| `$value` | **string&#124;string[]** | If set, the value of the above named attribute. If an array is given<br />all of its values will be allowed in the selector. |
| `$caseSensitive` | **bool** | If false, attribute values are matched case insensitively.<br />(This is not completely true, as only full upper or lower case strings are matched, not mixed case.<br />A lower-case function is missing in XPath 1.0.) |





***

### loadXPathFromItem

Load an XML file from the EPUB/ZIP archive into a new XPath object.

```php
protected loadXPathFromItem(string $path): \SebLucas\EPubMeta\Dom\XPath
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** | The XML file to load from the ZIP archive. |


**Return Value:**

The XPath representation of the XML file.



**Throws:**
<p>If the given path could not be read.</p>

- [`Exception`](../../Exception.md)



***

### getZipEntries

Get the stat entries for all files in a ZIP file

```php
public getZipEntries(string $file = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** | &amp;#124;null Path to a ZIP file or null for current file |


**Return Value:**

(filename => details of the entry)




***

### loadSizeMap

Map the items of a ZIP file to their respective file sizes.

```php
protected loadSizeMap(string $file = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** | &amp;#124;null Path to a ZIP file or null for current ZIP file |


**Return Value:**

(filename => file size)




***

### getImageCount



```php
public getImageCount(): int
```












***


***
> Automatically generated on 2025-03-18
