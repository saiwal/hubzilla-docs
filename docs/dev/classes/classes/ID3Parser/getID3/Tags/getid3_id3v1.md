***

# getid3_id3v1





* Full name: `\ID3Parser\getID3\Tags\getid3_id3v1`
* Parent class: [`\ID3Parser\getID3\getid3_handler`](../getid3_handler.md)




## Methods


### Analyze



```php
public Analyze(): mixed
```












***

### cutfield



```php
public static cutfield(mixed $str): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### ArrayOfGenres



```php
public static ArrayOfGenres(mixed $allowSCMPXextended = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$allowSCMPXextended` | **mixed** |  |





***

### LookupGenreName



```php
public static LookupGenreName(mixed $genreid, mixed $allowSCMPXextended = true): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$genreid` | **mixed** |  |
| `$allowSCMPXextended` | **mixed** |  |





***

### LookupGenreID



```php
public static LookupGenreID(mixed $genre, mixed $allowSCMPXextended = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$genre` | **mixed** |  |
| `$allowSCMPXextended` | **mixed** |  |





***

### StandardiseID3v1GenreName



```php
public static StandardiseID3v1GenreName(mixed $OriginalGenre): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$OriginalGenre` | **mixed** |  |





***

### GenerateID3v1Tag



```php
public static GenerateID3v1Tag(mixed $title, mixed $artist, mixed $album, mixed $year, mixed $genreid, mixed $comment, mixed $track = &#039;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$title` | **mixed** |  |
| `$artist` | **mixed** |  |
| `$album` | **mixed** |  |
| `$year` | **mixed** |  |
| `$genreid` | **mixed** |  |
| `$comment` | **mixed** |  |
| `$track` | **mixed** |  |





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
