
# SimplePie_Item

Manages all item-related data



* Full name: `\SimplePie_Item`
* Parent class: [`\SimplePie\Item`](./SimplePie/Item.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct

Create a new item object

```php
public __construct(\SimplePie\SimplePie $feed, array $data): mixed
```

This is usually used by {@see \SimplePie\SimplePie::get_items} and
{@see \SimplePie\SimplePie::get_item}. Avoid creating this manually.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$feed` | **\SimplePie\SimplePie** | Parent feed |
| `$data` | **array** | Raw data |





***

### set_registry

Set the registry handler

```php
public set_registry(\SimplePie\Registry $registry): void
```

This is usually used by {@see \SimplePie\Registry::create}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$registry` | **\SimplePie\Registry** |  |





***

### __toString

Get a string representation of the item

```php
public __toString(): string
```












***

### __destruct

Remove items that link back to this before destroying this object

```php
public __destruct(): mixed
```












***

### get_item_tags

Get data for an item-level element

```php
public get_item_tags(string $namespace, string $tag): array
```

This method allows you to get access to ANY element/attribute that is a
sub-element of the item/entry tag.

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

Get the base URL value.

```php
public get_base(array $element = []): string
```

Uses `<xml:base>`, or item link, or feed base URL.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **array** |  |





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

* \SimplePie\SimplePie::sanitize() - 

***

### get_feed

Get the parent feed

```php
public get_feed(): \SimplePie\SimplePie
```

Note: this may not work as you think for multifeeds!










**See Also:**

* http://simplepie.org/faq/typical_multifeed_gotchas#missing_data_from_feed - 

***

### get_id

Get the unique identifier for the item

```php
public get_id(bool $hash = false, string|false $fn = &#039;md5&#039;): string|null
```

This is usually used when writing code to check for new items in a feed.

Uses `<atom:id>`, `<guid>`, `<dc:identifier>` or the `about` attribute
for RDF. If none of these are supplied (or `$hash` is true), creates an
MD5 hash based on the permalink, title and content.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **bool** | Should we force using a hash instead of the supplied ID? |
| `$fn` | **string&#124;false** | User-supplied function to generate an hash |





***

### get_title

Get the title of the item

```php
public get_title(): string|null
```

Uses `<atom:title>`, `<title>` or `<dc:title>`










***

### get_description

Get the content for the item

```php
public get_description(bool $description_only = false): string|null
```

Prefers summaries over full content , but will return full content if a
summary does not exist.

To prefer full content instead, use {@see \SimplePie\get_content}

Uses `<atom:summary>`, `<description>`, `<dc:description>` or
`<itunes:subtitle>`






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$description_only` | **bool** | Should we avoid falling back to the content? |





***

### get_content

Get the content for the item

```php
public get_content(bool $content_only = false): string|null
```

Prefers full content over summaries, but will return a summary if full
content does not exist.

To prefer summaries instead, use {@see \SimplePie\get_description}

Uses `<atom:content>` or `<content:encoded>` (RSS 1.0 Content Module)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content_only` | **bool** | Should we avoid falling back to the description? |





***

### get_thumbnail

Get the media:thumbnail of the item

```php
public get_thumbnail(): array|null
```

Uses `<media:thumbnail>`










***

### get_category

Get a category for the item

```php
public get_category(int $key): \SimplePie\Category|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The category that you want to return.  Remember that arrays begin with 0, not 1 |





***

### get_categories

Get all categories for the item

```php
public get_categories(): \SimplePie\Category[]|null
```

Uses `<atom:category>`, `<category>` or `<dc:subject>`







**Return Value:**

List of {@see \SimplePie\Category} objects




***

### get_author

Get an author for the item

```php
public get_author(int $key): \SimplePie\Author|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The author that you want to return.  Remember that arrays begin with 0, not 1 |





***

### get_contributor

Get a contributor for the item

```php
public get_contributor(int $key): \SimplePie\Author|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The contrbutor that you want to return.  Remember that arrays begin with 0, not 1 |





***

### get_contributors

Get all contributors for the item

```php
public get_contributors(): \SimplePie\Author[]|null
```

Uses `<atom:contributor>`







**Return Value:**

List of {@see \SimplePie\Author} objects




***

### get_authors

Get all authors for the item

```php
public get_authors(): \SimplePie\Author[]|null
```

Uses `<atom:author>`, `<author>`, `<dc:creator>` or `<itunes:author>`







**Return Value:**

List of {@see \SimplePie\Author} objects




***

### get_copyright

Get the copyright info for the item

```php
public get_copyright(): string
```

Uses `<atom:rights>` or `<dc:rights>`










***

### get_date

Get the posting date/time for the item

```php
public get_date(string $date_format = &#039;j F Y, g:i a&#039;): int|string|null
```

Uses `<atom:published>`, `<atom:updated>`, `<atom:issued>`,
`<atom:modified>`, `<pubDate>` or `<dc:date>`

Note: obeys PHP's timezone setting. To get a UTC date/time, use
{@see \SimplePie\get_gmdate}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date_format` | **string** | Supports any PHP date format from {@see http://php.net/date} (empty for the raw data) |





***

### get_updated_date

Get the update date/time for the item

```php
public get_updated_date(string $date_format = &#039;j F Y, g:i a&#039;): int|string|null
```

Uses `<atom:updated>`

Note: obeys PHP's timezone setting. To get a UTC date/time, use
{@see \SimplePie\get_gmdate}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date_format` | **string** | Supports any PHP date format from {@see http://php.net/date} (empty for the raw data) |





***

### get_local_date

Get the localized posting date/time for the item

```php
public get_local_date(string $date_format = &#039;%c&#039;): int|string|null
```

Returns the date formatted in the localized language. To display in
languages other than the server's default, you need to change the locale
with {@link http://php.net/setlocale}. The available
localizations depend on which ones are installed on your web server.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date_format` | **string** | Supports any PHP date format from {@see http://php.net/strftime} (empty for the raw data) |





***

### get_gmdate

Get the posting date/time for the item (UTC time)

```php
public get_gmdate(string $date_format = &#039;j F Y, g:i a&#039;): int|string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date_format` | **string** | Supports any PHP date format from {@see http://php.net/date} |





**See Also:**

* \SimplePie\get_date - 

***

### get_updated_gmdate

Get the update date/time for the item (UTC time)

```php
public get_updated_gmdate(string $date_format = &#039;j F Y, g:i a&#039;): int|string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$date_format` | **string** | Supports any PHP date format from {@see http://php.net/date} |





**See Also:**

* \SimplePie\get_updated_date - 

***

### get_permalink

Get the permalink for the item

```php
public get_permalink(): string|null
```

Returns the first link available with a relationship of "alternate".
Identical to {@see \SimplePie\get_link()} with key 0







**Return Value:**

Permalink URL




**See Also:**

* \SimplePie\get_link - 

***

### get_link

Get a single link for the item

```php
public get_link(int $key, string $rel = &#039;alternate&#039;): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The link that you want to return.  Remember that arrays begin with 0, not 1 |
| `$rel` | **string** | The relationship of the link to return |


**Return Value:**

Link URL




***

### get_links

Get all links for the item

```php
public get_links(string $rel = &#039;alternate&#039;): array|null
```

Uses `<atom:link>`, `<link>` or `<guid>`






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rel` | **string** | The relationship of links to return |


**Return Value:**

Links found for the item (strings)




***

### get_enclosure

Get an enclosure from the item

```php
public get_enclosure(int $key, mixed $prefer = null): \SimplePie\Enclosure|null
```

Supports the <enclosure> RSS tag, as well as Media RSS and iTunes RSS.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **int** | The enclosure that you want to return.  Remember that arrays begin with 0, not 1 |
| `$prefer` | **mixed** |  |





***

### get_enclosures

Get all available enclosures (podcasts, etc.)

```php
public get_enclosures(): \SimplePie\Enclosure[]|null
```

Supports the <enclosure> RSS tag, as well as Media RSS and iTunes RSS.

At this point, we're pretty much assuming that all enclosures for an item
are the same content.  Anything else is too complicated to
properly support.







**Return Value:**

List of \SimplePie\Enclosure items




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

Get the longitude coordinates for the item

```php
public get_longitude(): string|null
```

Compatible with the W3C WGS84 Basic Geo and GeoRSS specifications

Uses `<geo:long>`, `<geo:lon>` or `<georss:point>`










**See Also:**

* http://www.w3.org/2003/01/geo/ - W3C WGS84 Basic Geo* http://www.georss.org/ - GeoRSS

***

### get_source

Get the `<atom:source>` for the item

```php
public get_source(): \SimplePie\Source|null
```












***


***
> Automatically generated on 2025-03-18
