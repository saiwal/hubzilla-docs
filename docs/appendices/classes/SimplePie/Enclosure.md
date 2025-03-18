
# Enclosure

Handles everything related to enclosures (including Media RSS and iTunes RSS)

Used by {@see \SimplePie\Item::get_enclosure()} and {@see \SimplePie\Item::get_enclosures()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_enclosure_class()}

* Full name: `\SimplePie\Enclosure`



## Properties


### bitrate



```php
public string $bitrate
```





**See Also:**

* \SimplePie\get_bitrate() - 

***

### captions



```php
public array $captions
```





**See Also:**

* \SimplePie\get_captions() - 

***

### categories



```php
public array $categories
```





**See Also:**

* \SimplePie\get_categories() - 

***

### channels



```php
public int $channels
```





**See Also:**

* \SimplePie\get_channels() - 

***

### copyright



```php
public \SimplePie\Copyright $copyright
```





**See Also:**

* \SimplePie\get_copyright() - 

***

### credits



```php
public array $credits
```





**See Also:**

* \SimplePie\get_credits() - 

***

### description



```php
public string $description
```





**See Also:**

* \SimplePie\get_description() - 

***

### duration



```php
public int $duration
```





**See Also:**

* \SimplePie\get_duration() - 

***

### expression



```php
public string $expression
```





**See Also:**

* \SimplePie\get_expression() - 

***

### framerate



```php
public string $framerate
```





**See Also:**

* \SimplePie\get_framerate() - 

***

### handler



```php
public string $handler
```





**See Also:**

* \SimplePie\get_handler() - 

***

### hashes



```php
public array $hashes
```





**See Also:**

* \SimplePie\get_hashes() - 

***

### height



```php
public string $height
```





**See Also:**

* \SimplePie\get_height() - 

***

### javascript



```php
public null $javascript
```




* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### keywords



```php
public array $keywords
```





**See Also:**

* \SimplePie\get_keywords() - 

***

### lang



```php
public string $lang
```





**See Also:**

* \SimplePie\get_language() - 

***

### length



```php
public string $length
```





**See Also:**

* \SimplePie\get_length() - 

***

### link



```php
public string $link
```





**See Also:**

* \SimplePie\get_link() - 

***

### medium



```php
public string $medium
```





**See Also:**

* \SimplePie\get_medium() - 

***

### player



```php
public string $player
```





**See Also:**

* \SimplePie\get_player() - 

***

### ratings



```php
public array $ratings
```





**See Also:**

* \SimplePie\get_ratings() - 

***

### restrictions



```php
public array $restrictions
```





**See Also:**

* \SimplePie\get_restrictions() - 

***

### samplingrate



```php
public string $samplingrate
```





**See Also:**

* \SimplePie\get_sampling_rate() - 

***

### thumbnails



```php
public array $thumbnails
```





**See Also:**

* \SimplePie\get_thumbnails() - 

***

### title



```php
public string $title
```





**See Also:**

* \SimplePie\get_title() - 

***

### type



```php
public string $type
```





**See Also:**

* \SimplePie\get_type() - 

***

### width



```php
public string $width
```





**See Also:**

* \SimplePie\get_width() - 

***

## Methods


### __construct

Constructor, used to input the data

```php
public __construct(mixed $link = null, mixed $type = null, mixed $length = null, mixed $javascript = null, mixed $bitrate = null, mixed $captions = null, mixed $categories = null, mixed $channels = null, mixed $copyright = null, mixed $credits = null, mixed $description = null, mixed $duration = null, mixed $expression = null, mixed $framerate = null, mixed $hashes = null, mixed $height = null, mixed $keywords = null, mixed $lang = null, mixed $medium = null, mixed $player = null, mixed $ratings = null, mixed $restrictions = null, mixed $samplingrate = null, mixed $thumbnails = null, mixed $title = null, mixed $width = null): mixed
```

For documentation on all the parameters, see the corresponding
properties and their accessors






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$link` | **mixed** |  |
| `$type` | **mixed** |  |
| `$length` | **mixed** |  |
| `$javascript` | **mixed** |  |
| `$bitrate` | **mixed** |  |
| `$captions` | **mixed** |  |
| `$categories` | **mixed** |  |
| `$channels` | **mixed** |  |
| `$copyright` | **mixed** |  |
| `$credits` | **mixed** |  |
| `$description` | **mixed** |  |
| `$duration` | **mixed** |  |
| `$expression` | **mixed** |  |
| `$framerate` | **mixed** |  |
| `$hashes` | **mixed** |  |
| `$height` | **mixed** |  |
| `$keywords` | **mixed** |  |
| `$lang` | **mixed** |  |
| `$medium` | **mixed** |  |
| `$player` | **mixed** |  |
| `$ratings` | **mixed** |  |
| `$restrictions` | **mixed** |  |
| `$samplingrate` | **mixed** |  |
| `$thumbnails` | **mixed** |  |
| `$title` | **mixed** |  |
| `$width` | **mixed** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_bitrate

Get the bitrate

```php
public get_bitrate(): string|null
```












***

### get_caption

Get a single caption

```php
public get_caption(int $key): \SimplePie\Caption|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |





***

### get_captions

Get all captions

```php
public get_captions(): array|null
```









**Return Value:**

Array of {@see \SimplePie\Caption} objects




***

### get_category

Get a single category

```php
public get_category(int $key): \SimplePie\Category|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |





***

### get_categories

Get all categories

```php
public get_categories(): array|null
```









**Return Value:**

Array of {@see \SimplePie\Category} objects




***

### get_channels

Get the number of audio channels

```php
public get_channels(): int|null
```












***

### get_copyright

Get the copyright information

```php
public get_copyright(): \SimplePie\Copyright|null
```












***

### get_credit

Get a single credit

```php
public get_credit(int $key): \SimplePie\Credit|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |





***

### get_credits

Get all credits

```php
public get_credits(): array|null
```









**Return Value:**

Array of {@see \SimplePie\Credit} objects




***

### get_description

Get the description of the enclosure

```php
public get_description(): string|null
```












***

### get_duration

Get the duration of the enclosure

```php
public get_duration(bool $convert = false): string|int|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$convert` | **bool** | Convert seconds into hh:mm:ss |


**Return Value:**

'hh:mm:ss' string if `$convert` was specified, otherwise integer (or null if none found)




***

### get_expression

Get the expression

```php
public get_expression(): string
```









**Return Value:**

Probably one of 'sample', 'full', 'nonstop', 'clip'. Defaults to 'full'




***

### get_extension

Get the file extension

```php
public get_extension(): string|null
```












***

### get_framerate

Get the framerate (in frames-per-second)

```php
public get_framerate(): string|null
```












***

### get_handler

Get the preferred handler

```php
public get_handler(): string|null
```









**Return Value:**

One of 'flash', 'fmedia', 'quicktime', 'wmedia', 'mp3'




***

### get_hash

Get a single hash

```php
public get_hash(int $key): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |


**Return Value:**

Hash as per `media:hash`, prefixed with "$algo:"




**See Also:**

* http://www.rssboard.org/media-rss#media-hash - 

***

### get_hashes

Get all credits

```php
public get_hashes(): array|null
```









**Return Value:**

Array of strings, see {@see \SimplePie\get_hash()}




***

### get_height

Get the height

```php
public get_height(): string|null
```












***

### get_language

Get the language

```php
public get_language(): string|null
```









**Return Value:**

Language code as per RFC 3066




**See Also:**

* http://tools.ietf.org/html/rfc3066 - 

***

### get_keyword

Get a single keyword

```php
public get_keyword(int $key): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |





***

### get_keywords

Get all keywords

```php
public get_keywords(): array|null
```









**Return Value:**

Array of strings




***

### get_length

Get length

```php
public get_length(): float
```









**Return Value:**

Length in bytes




***

### get_link

Get the URL

```php
public get_link(): string|null
```












***

### get_medium

Get the medium

```php
public get_medium(): string|null
```









**Return Value:**

Should be one of 'image', 'audio', 'video', 'document', 'executable'




**See Also:**

* http://www.rssboard.org/media-rss#media-content - 

***

### get_player

Get the player URL

```php
public get_player(): string|null
```

Typically the same as {@see \SimplePie\get_permalink()}







**Return Value:**

Player URL




***

### get_rating

Get a single rating

```php
public get_rating(int $key): \SimplePie\Rating|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |





***

### get_ratings

Get all ratings

```php
public get_ratings(): array|null
```









**Return Value:**

Array of {@see \SimplePie\Rating} objects




***

### get_restriction

Get a single restriction

```php
public get_restriction(int $key): \SimplePie\Restriction|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |





***

### get_restrictions

Get all restrictions

```php
public get_restrictions(): array|null
```









**Return Value:**

Array of {@see \SimplePie\Restriction} objects




***

### get_sampling_rate

Get the sampling rate (in kHz)

```php
public get_sampling_rate(): string|null
```












***

### get_size

Get the file size (in MiB)

```php
public get_size(): float|null
```









**Return Value:**

File size in mebibytes (1048 bytes)




***

### get_thumbnail

Get a single thumbnail

```php
public get_thumbnail(int $key): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** |  |


**Return Value:**

Thumbnail URL




***

### get_thumbnails

Get all thumbnails

```php
public get_thumbnails(): array|null
```









**Return Value:**

Array of thumbnail URLs




***

### get_title

Get the title

```php
public get_title(): string|null
```












***

### get_type

Get mimetype of the enclosure

```php
public get_type(): string|null
```









**Return Value:**

MIME type




**See Also:**

* \SimplePie\get_real_type() - 

***

### get_width

Get the width

```php
public get_width(): string|null
```












***

### native_embed

Embed the enclosure using `<embed>`

```php
public native_embed(array|string $options = &#039;&#039;): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **array&#124;string** | See first parameter to {@see \SimplePie\embed} |


**Return Value:**

HTML string to output




***

### embed

Embed the enclosure using Javascript

```php
public embed(array|string $options = &#039;&#039;, bool $native = false): string
```

`$options` is an array or comma-separated key:value string, with the
following properties:

- `alt` (string): Alternate content for when an end-user does not have
   the appropriate handler installed or when a file type is
   unsupported. Can be any text or HTML. Defaults to blank.
- `altclass` (string): If a file type is unsupported, the end-user will
   see the alt text (above) linked directly to the content. That link
   will have this value as its class name. Defaults to blank.
- `audio` (string): This is an image that should be used as a
   placeholder for audio files before they're loaded (QuickTime-only).
   Can be any relative or absolute URL. Defaults to blank.
- `bgcolor` (string): The background color for the media, if not
   already transparent. Defaults to `#ffffff`.
- `height` (integer): The height of the embedded media. Accepts any
   numeric pixel value (such as `360`) or `auto`. Defaults to `auto`,
   and it is recommended that you use this default.
- `loop` (boolean): Do you want the media to loop when it's done?
   Defaults to `false`.
- `mediaplayer` (string): The location of the included
   `mediaplayer.swf` file. This allows for the playback of Flash Video
   (`.flv`) files, and is the default handler for non-Odeo MP3's.
   Defaults to blank.
- `video` (string): This is an image that should be used as a
   placeholder for video files before they're loaded (QuickTime-only).
   Can be any relative or absolute URL. Defaults to blank.
- `width` (integer): The width of the embedded media. Accepts any
   numeric pixel value (such as `480`) or `auto`. Defaults to `auto`,
   and it is recommended that you use this default.
- `widescreen` (boolean): Is the enclosure widescreen or standard?
   This applies only to video enclosures, and will automatically resize
   the content appropriately.  Defaults to `false`, implying 4:3 mode.

Note: Non-widescreen (4:3) mode with `width` and `height` set to `auto`
will default to 480x360 video resolution.  Widescreen (16:9) mode with
`width` and `height` set to `auto` will default to 480x270 video resolution.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **array&#124;string** | Comma-separated key:value list, or array |
| `$native` | **bool** | Use `&lt;embed&gt;` |


**Return Value:**

HTML string to output




***

### get_real_type

Get the real media type

```php
public get_real_type(bool $find_handler = false): string
```

Often, feeds lie to us, necessitating a bit of deeper inspection. This
converts types to their canonical representations based on the file
extension






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$find_handler` | **bool** | Internal use only, use {@see \SimplePie\get_handler()} instead |


**Return Value:**

MIME type




**See Also:**

* \SimplePie\get_type() - 

***


***
> Automatically generated on 2025-03-18
