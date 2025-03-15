***

# SimplePie

SimplePie



* Full name: `\SimplePie`
* Parent class: [`\SimplePie\SimplePie`](./SimplePie/SimplePie.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct

The SimplePie class contains feed level data and options

```php
public __construct(): mixed
```

To use SimplePie, create the SimplePie object with no parameters. You can
then set configuration options using the provided methods. After setting
them, you must initialise the feed using $feed->init(). At that point the
object's methods and properties will be available to you.

Previously, it was possible to pass in the feed URL along with cache
options directly into the constructor. This has been removed as of 1.3 as
it caused a lot of confusion.










***

### __toString

Used for converting object to a string

```php
public __toString(): mixed
```












***

### __destruct

Remove items that link back to this before destroying this object

```php
public __destruct(): mixed
```












***

### force_feed

Force the given data/URL to be treated as a feed

```php
public force_feed(bool $enable = false): mixed
```

This tells SimplePie to ignore the content-type provided by the server.
Be careful when using this option, as it will also disable autodiscovery.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **bool** | Force the given data/URL to be treated as a feed |





***

### set_feed_url

Set the URL of the feed you want to parse

```php
public set_feed_url(string|array $url): mixed
```

This allows you to enter the URL of the feed you want to parse, or the
website you want to try to use auto-discovery on. This takes priority
over any set raw data.

You can set multiple feeds to mash together by passing an array instead
of a string for the $url. Remember that with each additional feed comes
additional processing and resources.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string&#124;array** | This is the URL (or array of URLs) that you want to parse. |





**See Also:**

* \SimplePie\set_raw_data() - 

***

### set_file

Set an instance of {@see \SimplePie\File} to use as a feed

```php
public set_file(\SimplePie\File& $file): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **\SimplePie\File** |  |


**Return Value:**

True on success, false on failure




***

### set_raw_data

Set the raw XML data to parse

```php
public set_raw_data(string $data): mixed
```

Allows you to use a string of RSS/Atom data instead of a remote feed.

If you have a feed available as a string in PHP, you can tell SimplePie
to parse that data string instead of a remote feed. Any set feed URL
takes precedence.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | RSS or Atom data as a string. |





**See Also:**

* \SimplePie\set_feed_url() - 

***

### set_timeout

Set the default timeout for fetching remote feeds

```php
public set_timeout(int $timeout = 10): mixed
```

This allows you to change the maximum time the feed's server to respond
and send the feed back.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timeout` | **int** | The maximum number of seconds to spend waiting to retrieve a feed. |





***

### set_curl_options

Set custom curl options

```php
public set_curl_options(array $curl_options = []): mixed
```

This allows you to change default curl options






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$curl_options` | **array** | Curl options to add to default settings |





***

### force_fsockopen

Force SimplePie to use fsockopen() instead of cURL

```php
public force_fsockopen(bool $enable = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **bool** | Force fsockopen() to be used |





***

### enable_cache

Enable/disable caching in SimplePie.

```php
public enable_cache(bool $enable = true): mixed
```

This option allows you to disable caching all-together in SimplePie.
However, disabling the cache can lead to longer load times.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **bool** | Enable caching |





***

### set_cache

Set a PSR-16 implementation as cache

```php
public set_cache(\Psr\SimpleCache\CacheInterface $cache): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cache` | **\Psr\SimpleCache\CacheInterface** |  |





***

### force_cache_fallback

SimplePie to continue to fall back to expired cache, if enabled, when
feed is unavailable.

```php
public force_cache_fallback(bool $enable = false): mixed
```

This tells SimplePie to ignore any file errors and fall back to cache
instead. This only works if caching is enabled and cached content
still exists.




* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **bool** | Force use of cache on fail. |





***

### set_cache_duration

Set the length of time (in seconds) that the contents of a feed will be
cached

```php
public set_cache_duration(int $seconds = 3600): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$seconds` | **int** | The feed content cache duration |





***

### set_autodiscovery_cache_duration

Set the length of time (in seconds) that the autodiscovered feed URL will
be cached

```php
public set_autodiscovery_cache_duration(int $seconds = 604800): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$seconds` | **int** | The autodiscovered feed URL cache duration. |





***

### set_cache_location

Set the file system location where the cached files should be stored

```php
public set_cache_location(string $location = &#039;./cache&#039;): mixed
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **string** | The file system location. |





***

### get_cache_filename

Return the filename (i.e. hash, without path and without extension) of the file to cache a given URL.

```php
public get_cache_filename(string $url): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** | The URL of the feed to be cached. |


**Return Value:**

A filename (i.e. hash, without path and without extension).




***

### enable_order_by_date

Set whether feed items should be sorted into reverse chronological order

```php
public enable_order_by_date(bool $enable = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **bool** | Sort as reverse chronological order. |





***

### set_input_encoding

Set the character encoding used to parse the feed

```php
public set_input_encoding(string $encoding = false): mixed
```

This overrides the encoding reported by the feed, however it will fall
back to the normal encoding detection if the override fails






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **string** | Character encoding |





***

### set_autodiscovery_level

Set how much feed autodiscovery to do

```php
public set_autodiscovery_level(int $level = self::LOCATOR_ALL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$level` | **int** | Feed Autodiscovery Level (level can be a combination of the above constants, see bitwise OR operator) |





**See Also:**

* \SimplePie\SimplePie::LOCATOR_NONE - * \SimplePie\SimplePie::LOCATOR_AUTODISCOVERY - * \SimplePie\SimplePie::LOCATOR_LOCAL_EXTENSION - * \SimplePie\SimplePie::LOCATOR_LOCAL_BODY - * \SimplePie\SimplePie::LOCATOR_REMOTE_EXTENSION - * \SimplePie\SimplePie::LOCATOR_REMOTE_BODY - * \SimplePie\SimplePie::LOCATOR_ALL - 

***

### get_registry

Get the class registry

```php
public get_registry(): \SimplePie\Registry
```

Use this to override SimplePie's default classes










**See Also:**

* \SimplePie\Registry - 

***

### set_cache_class

Set which class SimplePie uses for caching

```php
public set_cache_class(string $class = Cache::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_locator_class

Set which class SimplePie uses for auto-discovery

```php
public set_locator_class(string $class = Locator::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_parser_class

Set which class SimplePie uses for XML parsing

```php
public set_parser_class(string $class = Parser::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_file_class

Set which class SimplePie uses for remote file fetching

```php
public set_file_class(string $class = File::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_sanitize_class

Set which class SimplePie uses for data sanitization

```php
public set_sanitize_class(string $class = Sanitize::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_item_class

Set which class SimplePie uses for handling feed items

```php
public set_item_class(string $class = Item::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_author_class

Set which class SimplePie uses for handling author data

```php
public set_author_class(string $class = Author::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_category_class

Set which class SimplePie uses for handling category data

```php
public set_category_class(string $class = Category::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_enclosure_class

Set which class SimplePie uses for feed enclosures

```php
public set_enclosure_class(string $class = Enclosure::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_caption_class

Set which class SimplePie uses for `<media:text>` captions

```php
public set_caption_class(string $class = Caption::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_copyright_class

Set which class SimplePie uses for `<media:copyright>`

```php
public set_copyright_class(string $class = Copyright::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_credit_class

Set which class SimplePie uses for `<media:credit>`

```php
public set_credit_class(string $class = Credit::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_rating_class

Set which class SimplePie uses for `<media:rating>`

```php
public set_rating_class(string $class = Rating::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_restriction_class

Set which class SimplePie uses for `<media:restriction>`

```php
public set_restriction_class(string $class = Restriction::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_content_type_sniffer_class

Set which class SimplePie uses for content-type sniffing

```php
public set_content_type_sniffer_class(string $class = Sniffer::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_source_class

Set which class SimplePie uses item sources

```php
public set_source_class(string $class = Source::class): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | Name of custom class |


**Return Value:**

True on success, false otherwise




***

### set_useragent

Set the user agent string

```php
public set_useragent(string $ua = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ua` | **string** | New user agent string. |





***

### set_cache_namefilter

Set a namefilter to modify the cache filename with

```php
public set_cache_namefilter(\SimplePie\Cache\NameFilter $filter): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filter` | **\SimplePie\Cache\NameFilter** |  |





***

### set_cache_name_function

Set callback function to create cache filename with

```php
public set_cache_name_function(mixed $function = &#039;md5&#039;): mixed
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$function` | **mixed** | Callback function |





***

### set_stupidly_fast

Set options to make SP as fast as possible

```php
public set_stupidly_fast(bool $set = false): mixed
```

Forgoes a substantial amount of data sanitization in favor of speed. This
turns SimplePie into a dumb parser of feeds.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$set` | **bool** | Whether to set them or not |





***

### set_max_checked_feeds

Set maximum number of feeds to check with autodiscovery

```php
public set_max_checked_feeds(int $max = 10): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$max` | **int** | Maximum number of feeds to check |





***

### remove_div



```php
public remove_div(mixed $enable = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **mixed** |  |





***

### strip_htmltags



```php
public strip_htmltags(mixed $tags = &#039;&#039;, mixed $encode = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tags` | **mixed** |  |
| `$encode` | **mixed** |  |





***

### encode_instead_of_strip



```php
public encode_instead_of_strip(mixed $enable = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **mixed** |  |





***

### rename_attributes



```php
public rename_attributes(mixed $attribs = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### strip_attributes



```php
public strip_attributes(mixed $attribs = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### add_attributes



```php
public add_attributes(mixed $attribs = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### set_output_encoding

Set the output encoding

```php
public set_output_encoding(string $encoding = &#039;UTF-8&#039;): mixed
```

Allows you to override SimplePie's output to match that of your webpage.
This is useful for times when your webpages are not being served as
UTF-8. This setting will be obeyed by {@see \SimplePie\handle_content_type()}, and
is similar to {@see \SimplePie\set_input_encoding()}.

It should be noted, however, that not all character encodings can support
all characters. If your page is being served as ISO-8859-1 and you try
to display a Japanese feed, you'll likely see garbled characters.
Because of this, it is highly recommended to ensure that your webpages
are served as UTF-8.

The number of supported character encodings depends on whether your web
host supports {@link http://php.net/mbstring},
{@link http://php.net/iconv}, or both. See
{@link http://simplepie.org/wiki/faq/Supported_Character_Encodings} for
more information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **string** |  |





***

### strip_comments



```php
public strip_comments(mixed $strip = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$strip` | **mixed** |  |





***

### set_url_replacements

Set element/attribute key/value pairs of HTML attributes
containing URLs that need to be resolved relative to the feed

```php
public set_url_replacements(array|null $element_attribute = null): mixed
```

Defaults to |a|@href, |area|@href, |blockquote|@cite, |del|@cite,
|form|@action, |img|@longdesc, |img|@src, |input|@src, |ins|@cite,
|q|@cite






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element_attribute` | **array&#124;null** | Element/attribute key/value pairs, null for default |





***

### set_https_domains

Set the list of domains for which to force HTTPS.

```php
public set_https_domains(mixed $domains = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$domains` | **mixed** |  |





**See Also:**

* \SimplePie\Sanitize::set_https_domains() - 

***

### set_image_handler

Set the handler to enable the display of cached images.

```php
public set_image_handler(string $page = false, string $qs = &#039;i&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$page` | **string** | Web-accessible path to the handler_image.php file. |
| `$qs` | **string** | The query string that the value should be passed to. |





***

### set_item_limit

Set the limit for items returned per-feed with multifeeds

```php
public set_item_limit(int $limit): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$limit` | **int** | The maximum number of items to return. |





***

### enable_exceptions

Enable throwing exceptions

```php
public enable_exceptions(bool $enable = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable` | **bool** | Should we throw exceptions, or use the old-style error property? |





***

### init

Initialize the feed object

```php
public init(): bool
```

This is what makes everything happen. Period. This is where all of the
configuration options get processed, feeds are fetched, cached, and
parsed, and all of that other good stuff.







**Return Value:**

True if successful, false otherwise




***

### fetch_data

Fetch the data via \SimplePie\File

```php
protected fetch_data(\SimplePie\Cache\Base|\SimplePie\Cache\DataCache|false& $cache): array|true
```

If the data is already cached, attempt to fetch it from there instead






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cache` | **\SimplePie\Cache\Base&#124;\SimplePie\Cache\DataCache&#124;false** | Cache handler, or false to not load from the cache |


**Return Value:**

Returns true if the data was loaded from the cache, or an array of HTTP headers and sniffed type




***

### error

Get the error message for the occurred error

```php
public error(): string|array
```









**Return Value:**

Error message, or array of messages for multifeeds




***

### status_code

Get the last HTTP status code

```php
public status_code(): int
```









**Return Value:**

Status code




***

### get_raw_data

Get the raw XML

```php
public get_raw_data(): string|bool
```

This is the same as the old `$feed->enable_xml_dump(true)`, but returns
the data instead of printing it.







**Return Value:**

Raw XML data, false if the cache is used




***

### get_encoding

Get the character encoding used for output

```php
public get_encoding(): string
```












***

### handle_content_type

Send the content-type header with correct encoding

```php
public handle_content_type(string $mime = &#039;text/html&#039;): mixed
```

This method ensures that the SimplePie-enabled page is being served with
the correct {@link http://www.iana.org/assignments/media-types/}
and character encoding HTTP headers (character encoding determined by the
{@see \SimplePie\set_output_encoding} config option).

This won't work properly if any content or whitespace has already been
sent to the browser, because it relies on PHP's
{@link http://php.net/header} function, and these are the
circumstances under which the function works.

Because it's setting these settings for the entire page (as is the nature
of HTTP headers), this should only be used once per page (again, at the
top).






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mime` | **string** | MIME type to serve the page as |





***

### get_type

Get the type of the feed

```php
public get_type(): int
```

This returns a \SimplePie\SimplePie::TYPE_* constant, which can be tested against
using {@link http://php.net/language.operators.bitwise}







**Return Value:**

\SimplePie\SimplePie::TYPE_* constant




**See Also:**

* \SimplePie\SimplePie::TYPE_NONE - Unknown.* \SimplePie\SimplePie::TYPE_RSS_090 - RSS 0.90.* \SimplePie\SimplePie::TYPE_RSS_091_NETSCAPE - RSS 0.91 (Netscape).* \SimplePie\SimplePie::TYPE_RSS_091_USERLAND - RSS 0.91 (Userland).* \SimplePie\SimplePie::TYPE_RSS_091 - RSS 0.91.* \SimplePie\SimplePie::TYPE_RSS_092 - RSS 0.92.* \SimplePie\SimplePie::TYPE_RSS_093 - RSS 0.93.* \SimplePie\SimplePie::TYPE_RSS_094 - RSS 0.94.* \SimplePie\SimplePie::TYPE_RSS_10 - RSS 1.0.* \SimplePie\SimplePie::TYPE_RSS_20 - RSS 2.0.x.* \SimplePie\SimplePie::TYPE_RSS_RDF - RDF-based RSS.* \SimplePie\SimplePie::TYPE_RSS_SYNDICATION - Non-RDF-based RSS (truly intended as syndication format).* \SimplePie\SimplePie::TYPE_RSS_ALL - Any version of RSS.* \SimplePie\SimplePie::TYPE_ATOM_03 - Atom 0.3.* \SimplePie\SimplePie::TYPE_ATOM_10 - Atom 1.0.* \SimplePie\SimplePie::TYPE_ATOM_ALL - Any version of Atom.* \SimplePie\SimplePie::TYPE_ALL - Any known/supported feed type.

***

### subscribe_url

Get the URL for the feed

```php
public subscribe_url(bool $permanent = false): string|null
```

When the 'permanent' mode is enabled, returns the original feed URL,
except in the case of an `HTTP 301 Moved Permanently` status response,
in which case the location of the first redirection is returned.

When the 'permanent' mode is disabled (default),
may or may not be different from the URL passed to {@see \SimplePie\set_feed_url()},
depending on whether auto-discovery was used, and whether there were
any redirects along the way.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$permanent` | **bool** | Permanent mode to return only the original URL or the first redirection<br />iff it is a 301 redirection |





***

### get_feed_tags

Get data for an feed-level element

```php
public get_feed_tags(string $namespace, string $tag): array
```

This method allows you to get access to ANY element/attribute that is a
sub-element of the opening feed tag.

The return value is an indexed array of elements matching the given
namespace and tag name. Each element has `attribs`, `data` and `child`
subkeys. For `attribs` and `child`, these contain namespace subkeys.
`attribs` then has one level of associative name => value data (where
`value` is a string) after the namespace. `child` has tag-indexed keys
after the namespace, each member of which is an indexed array matching
this same format.

For example:
<pre>
// This is probably a bad example because we already support
// <media:content> natively, but it shows you how to parse through
// the nodes.
$group = $item->get_item_tags(\SimplePie\SimplePie::NAMESPACE_MEDIARSS, 'group');
$content = $group[0]['child'][\SimplePie\SimplePie::NAMESPACE_MEDIARSS]['content'];
$file = $content[0]['attribs']['']['url'];
echo $file;
</pre>






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$namespace` | **string** | The URL of the XML namespace of the elements you&#039;re trying to access |
| `$tag` | **string** | Tag name |





**See Also:**

* http://simplepie.org/wiki/faq/supported_xml_namespaces - 

***

### get_channel_tags

Get data for an channel-level element

```php
public get_channel_tags(string $namespace, string $tag): array
```

This method allows you to get access to ANY element/attribute in the
channel/header section of the feed.

See {@see \SimplePie\SimplePie::get_feed_tags()} for a description of the return value






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$namespace` | **string** | The URL of the XML namespace of the elements you&#039;re trying to access |
| `$tag` | **string** | Tag name |





**See Also:**

* http://simplepie.org/wiki/faq/supported_xml_namespaces - 

***

### get_image_tags

Get data for an channel-level element

```php
public get_image_tags(string $namespace, string $tag): array
```

This method allows you to get access to ANY element/attribute in the
image/logo section of the feed.

See {@see \SimplePie\SimplePie::get_feed_tags()} for a description of the return value






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$namespace` | **string** | The URL of the XML namespace of the elements you&#039;re trying to access |
| `$tag` | **string** | Tag name |





**See Also:**

* http://simplepie.org/wiki/faq/supported_xml_namespaces - 

***

### get_base

Get the base URL value from the feed

```php
public get_base(array $element = []): string
```

Uses `<xml:base>` if available, otherwise uses the first link in the
feed, or failing that, the URL of the feed itself.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **array** |  |





**See Also:**

* \SimplePie\get_link - * \SimplePie\subscribe_url - 

***

### sanitize

Sanitize feed data

```php
public sanitize(string $data, int $type, string $base = &#039;&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Data to sanitize |
| `$type` | **int** | One of the \SimplePie\SimplePie::CONSTRUCT_* constants |
| `$base` | **string** | Base URL to resolve URLs against |


**Return Value:**

Sanitized data




**See Also:**

* \SimplePie\Sanitize::sanitize() - 

***

### get_title

Get the title of the feed

```php
public get_title(): string|null
```

Uses `<atom:title>`, `<title>` or `<dc:title>`










***

### get_category

Get a category for the feed

```php
public get_category(int $key): \SimplePie\Category|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The category that you want to return. Remember that arrays begin with 0, not 1 |





***

### get_categories

Get all categories for the feed

```php
public get_categories(): array|null
```

Uses `<atom:category>`, `<category>` or `<dc:subject>`







**Return Value:**

List of {@see \SimplePie\Category} objects




***

### get_author

Get an author for the feed

```php
public get_author(int $key): \SimplePie\Author|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The author that you want to return. Remember that arrays begin with 0, not 1 |





***

### get_authors

Get all authors for the feed

```php
public get_authors(): array|null
```

Uses `<atom:author>`, `<author>`, `<dc:creator>` or `<itunes:author>`







**Return Value:**

List of {@see \SimplePie\Author} objects




***

### get_contributor

Get a contributor for the feed

```php
public get_contributor(int $key): \SimplePie\Author|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The contrbutor that you want to return. Remember that arrays begin with 0, not 1 |





***

### get_contributors

Get all contributors for the feed

```php
public get_contributors(): array|null
```

Uses `<atom:contributor>`







**Return Value:**

List of {@see \SimplePie\Author} objects




***

### get_link

Get a single link for the feed

```php
public get_link(int $key, string $rel = &#039;alternate&#039;): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The link that you want to return. Remember that arrays begin with 0, not 1 |
| `$rel` | **string** | The relationship of the link to return |


**Return Value:**

Link URL




***

### get_links

Get all links for the feed

```php
public get_links(string $rel = &#039;alternate&#039;): array|null
```

Uses `<atom:link>` or `<link>`






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rel` | **string** | The relationship of links to return |


**Return Value:**

Links found for the feed (strings)




***

### get_all_discovered_feeds



```php
public get_all_discovered_feeds(): mixed
```












***

### get_description

Get the content for the item

```php
public get_description(): string|null
```

Uses `<atom:subtitle>`, `<atom:tagline>`, `<description>`,
`<dc:description>`, `<itunes:summary>` or `<itunes:subtitle>`










***

### get_copyright

Get the copyright info for the feed

```php
public get_copyright(): string|null
```

Uses `<atom:rights>`, `<atom:copyright>` or `<dc:rights>`










***

### get_language

Get the language for the feed

```php
public get_language(): string|null
```

Uses `<language>`, `<dc:language>`, or @xml_lang










***

### get_latitude

Get the latitude coordinates for the item

```php
public get_latitude(): string|null
```

Compatible with the W3C WGS84 Basic Geo and GeoRSS specifications

Uses `<geo:lat>` or `<georss:point>`










**See Also:**

* http://www.w3.org/2003/01/geo/ - W3C WGS84 Basic Geo* http://www.georss.org/ - GeoRSS

***

### get_longitude

Get the longitude coordinates for the feed

```php
public get_longitude(): string|null
```

Compatible with the W3C WGS84 Basic Geo and GeoRSS specifications

Uses `<geo:long>`, `<geo:lon>` or `<georss:point>`










**See Also:**

* http://www.w3.org/2003/01/geo/ - W3C WGS84 Basic Geo* http://www.georss.org/ - GeoRSS

***

### get_image_title

Get the feed logo's title

```php
public get_image_title(): string|null
```

RSS 0.9.0, 1.0 and 2.0 feeds are allowed to have a "feed logo" title.

Uses `<image><title>` or `<image><dc:title>`










***

### get_image_url

Get the feed logo's URL

```php
public get_image_url(): string|null
```

RSS 0.9.0, 2.0, Atom 1.0, and feeds with iTunes RSS tags are allowed to
have a "feed logo" URL. This points directly to the image itself.

Uses `<itunes:image>`, `<atom:logo>`, `<atom:icon>`,
`<image><title>` or `<image><dc:title>`










***

### get_image_link

Get the feed logo's link

```php
public get_image_link(): string|null
```

RSS 0.9.0, 1.0 and 2.0 feeds are allowed to have a "feed logo" link. This
points to a human-readable page that the image should link to.

Uses `<itunes:image>`, `<atom:logo>`, `<atom:icon>`,
`<image><title>` or `<image><dc:title>`










***

### get_image_width

Get the feed logo's link

```php
public get_image_width(): int|null
```

RSS 2.0 feeds are allowed to have a "feed logo" width.

Uses `<image><width>` or defaults to 88 if no width is specified and
the feed is an RSS 2.0 feed.










***

### get_image_height

Get the feed logo's height

```php
public get_image_height(): int|null
```

RSS 2.0 feeds are allowed to have a "feed logo" height.

Uses `<image><height>` or defaults to 31 if no height is specified and
the feed is an RSS 2.0 feed.










***

### get_item_quantity

Get the number of items in the feed

```php
public get_item_quantity(int $max): int
```

This is well-suited for {@link http://php.net/for} loops with
{@see \SimplePie\get_item()}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$max` | **int** | Maximum value to return. 0 for no limit |


**Return Value:**

Number of items in the feed




***

### get_item

Get a single item from the feed

```php
public get_item(int $key): \SimplePie\Item|null
```

This is better suited for {@link http://php.net/for} loops, whereas
{@see \SimplePie\get_items()} is better suited for
{@link http://php.net/foreach} loops.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The item that you want to return. Remember that arrays begin with 0, not 1 |





**See Also:**

* \SimplePie\get_item_quantity() - 

***

### get_items

Get all items from the feed

```php
public get_items(int $start, int $end): \SimplePie\Item[]|null
```

This is better suited for {@link http://php.net/for} loops, whereas
{@see \SimplePie\get_items()} is better suited for
{@link http://php.net/foreach} loops.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$start` | **int** | Index to start at |
| `$end` | **int** | Number of items to return. 0 for all items after `$start` |


**Return Value:**

List of {@see \SimplePie\Item} objects




**See Also:**

* \SimplePie\get_item_quantity - 

***

### set_favicon_handler

Set the favicon handler

```php
public set_favicon_handler(mixed $page = false, mixed $qs = &#039;i&#039;): mixed
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$page` | **mixed** |  |
| `$qs` | **mixed** |  |





***

### get_favicon

Get the favicon for the current feed

```php
public get_favicon(): mixed
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### __call

Magic method handler

```php
public __call(string $method, array $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **string** | Method name |
| `$args` | **array** | Arguments to the method |





***

### sort_items

Sorting callback for items

```php
public static sort_items(\SimplePie\SimplePie $a, \SimplePie\SimplePie $b): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **\SimplePie\SimplePie** |  |
| `$b` | **\SimplePie\SimplePie** |  |





***

### merge_items

Merge items from several feeds into one

```php
public static merge_items(array $urls, int $start, int $end, int $limit): array
```

If you're merging multiple feeds together, they need to all have dates
for the items or else SimplePie will refuse to sort them.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$urls` | **array** | List of SimplePie feed objects to merge |
| `$start` | **int** | Starting item |
| `$end` | **int** | Number of items to return |
| `$limit` | **int** | Maximum number of items per feed |





**See Also:**

* http://simplepie.org/wiki/tutorial/sort_multiple_feeds_by_time_and_date#if_feeds_require_separate_per-feed_settings - 

***

### store_links

Store PubSubHubbub links as headers

```php
private store_links(\SimplePie\File& $file, string $hub, string $self): mixed
```

There is no way to find PuSH links in the body of a microformats feed,
so they are added to the headers when found, to be used later by get_links.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **\SimplePie\File** |  |
| `$hub` | **string** |  |
| `$self` | **string** |  |





***

### get_cache

Get a DataCache

```php
private get_cache(string $feed_url = &#039;&#039;): \SimplePie\Cache\DataCache
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$feed_url` | **string** | Only needed for BC, can be removed in SimplePie 2.0.0 |





***


***
> Automatically generated on 2025-03-15
