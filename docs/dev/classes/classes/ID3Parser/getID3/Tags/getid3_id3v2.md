***

# getid3_id3v2





* Full name: `\ID3Parser\getID3\Tags\getid3_id3v2`
* Parent class: [`\ID3Parser\getID3\getid3_handler`](../getid3_handler.md)



## Properties


### StartingOffset



```php
public $StartingOffset
```






***

## Methods


### Analyze



```php
public Analyze(): mixed
```












***

### ParseID3v2GenreString



```php
public ParseID3v2GenreString(mixed $genrestring): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$genrestring` | **mixed** |  |





***

### ParseID3v2Frame



```php
public ParseID3v2Frame(mixed& $parsedFrame): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parsedFrame` | **mixed** |  |





***

### DeUnsynchronise



```php
public DeUnsynchronise(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### LookupExtendedHeaderRestrictionsTagSizeLimits



```php
public LookupExtendedHeaderRestrictionsTagSizeLimits(mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### LookupExtendedHeaderRestrictionsTextEncodings



```php
public LookupExtendedHeaderRestrictionsTextEncodings(mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### LookupExtendedHeaderRestrictionsTextFieldSize



```php
public LookupExtendedHeaderRestrictionsTextFieldSize(mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### LookupExtendedHeaderRestrictionsImageEncoding



```php
public LookupExtendedHeaderRestrictionsImageEncoding(mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### LookupExtendedHeaderRestrictionsImageSizeSize



```php
public LookupExtendedHeaderRestrictionsImageSizeSize(mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### LookupCurrencyUnits



```php
public LookupCurrencyUnits(mixed $currencyid): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$currencyid` | **mixed** |  |





***

### LookupCurrencyCountry



```php
public LookupCurrencyCountry(mixed $currencyid): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$currencyid` | **mixed** |  |





***

### LanguageLookup



```php
public static LanguageLookup(mixed $languagecode, mixed $casesensitive = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$languagecode` | **mixed** |  |
| `$casesensitive` | **mixed** |  |





***

### ETCOEventLookup



```php
public static ETCOEventLookup(mixed $index): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### SYTLContentTypeLookup



```php
public static SYTLContentTypeLookup(mixed $index): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### APICPictureTypeLookup



```php
public static APICPictureTypeLookup(mixed $index, mixed $returnarray = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |
| `$returnarray` | **mixed** |  |





***

### COMRReceivedAsLookup



```php
public static COMRReceivedAsLookup(mixed $index): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### RVA2ChannelTypeLookup



```php
public static RVA2ChannelTypeLookup(mixed $index): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **mixed** |  |





***

### FrameNameLongLookup



```php
public static FrameNameLongLookup(mixed $framename): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$framename` | **mixed** |  |





***

### FrameNameShortLookup



```php
public static FrameNameShortLookup(mixed $framename): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$framename` | **mixed** |  |





***

### TextEncodingTerminatorLookup



```php
public static TextEncodingTerminatorLookup(mixed $encoding): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **mixed** |  |





***

### TextEncodingNameLookup



```php
public static TextEncodingNameLookup(mixed $encoding): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **mixed** |  |





***

### IsValidID3v2FrameName



```php
public static IsValidID3v2FrameName(mixed $framename, mixed $id3v2majorversion): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$framename` | **mixed** |  |
| `$id3v2majorversion` | **mixed** |  |





***

### IsANumber



```php
public static IsANumber(mixed $numberstring, mixed $allowdecimal = false, mixed $allownegative = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberstring` | **mixed** |  |
| `$allowdecimal` | **mixed** |  |
| `$allownegative` | **mixed** |  |





***

### IsValidDateStampString



```php
public static IsValidDateStampString(mixed $datestamp): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$datestamp` | **mixed** |  |





***

### ID3v2HeaderLength



```php
public static ID3v2HeaderLength(mixed $majorversion): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$majorversion` | **mixed** |  |





***


## Inherited methods


### __construct



```php
public __construct(\ID3Parser\getID3\getID3 $getid3, mixed $call_module = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$getid3` | **\ID3Parser\getID3\getID3** |  |
| `$call_module` | **mixed** |  |





***

### Analyze



```php
public Analyze(): mixed
```




* This method is **abstract**.







***

### AnalyzeString



```php
public AnalyzeString(mixed $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### setStringMode



```php
public setStringMode(mixed $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### ftell



```php
protected ftell(): mixed
```












***

### fread



```php
protected fread(mixed $bytes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **mixed** |  |





***

### fseek



```php
protected fseek(mixed $bytes, mixed $whence = SEEK_SET): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **mixed** |  |
| `$whence` | **mixed** |  |





***

### feof



```php
protected feof(): mixed
```












***

### isDependencyFor



```php
final protected isDependencyFor(mixed $module): mixed
```





* This method is **final**.


**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$module` | **mixed** |  |





***

### error



```php
protected error(mixed $text): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **mixed** |  |





***

### warning



```php
protected warning(mixed $text): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **mixed** |  |





***

### notice



```php
protected notice(mixed $text): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
