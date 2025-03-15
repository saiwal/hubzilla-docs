
# SimplePie_Sanitize

Used for data cleanup and post-processing



* Full name: `\SimplePie_Sanitize`
* Parent class: [`\SimplePie\Sanitize`](./SimplePie/Sanitize.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct



```php
public __construct(): mixed
```












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

### set_image_handler



```php
public set_image_handler(mixed $page = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$page` | **mixed** |  |





***

### set_registry

Set the Registry into the class

```php
public set_registry(\SimplePie\Registry $registry): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$registry` | **\SimplePie\Registry** |  |





***

### pass_cache_data



```php
public pass_cache_data(mixed $enable_cache = true, mixed $cache_location = &#039;./cache&#039;, mixed $cache_name_function = &#039;md5&#039;, mixed $cache_class = &#039;SimplePieCache&#039;, \SimplePie\Cache\DataCache $cache = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$enable_cache` | **mixed** |  |
| `$cache_location` | **mixed** |  |
| `$cache_name_function` | **mixed** |  |
| `$cache_class` | **mixed** |  |
| `$cache` | **\SimplePie\Cache\DataCache** |  |





***

### pass_file_data



```php
public pass_file_data(mixed $file_class = &#039;SimplePieFile&#039;, mixed $timeout = 10, mixed $useragent = &#039;&#039;, mixed $force_fsockopen = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_class` | **mixed** |  |
| `$timeout` | **mixed** |  |
| `$useragent` | **mixed** |  |
| `$force_fsockopen` | **mixed** |  |





***

### strip_htmltags



```php
public strip_htmltags(mixed $tags = [&#039;base&#039;, &#039;blink&#039;, &#039;body&#039;, &#039;doctype&#039;, &#039;embed&#039;, &#039;font&#039;, &#039;form&#039;, &#039;frame&#039;, &#039;frameset&#039;, &#039;html&#039;, &#039;iframe&#039;, &#039;input&#039;, &#039;marquee&#039;, &#039;meta&#039;, &#039;noscript&#039;, &#039;object&#039;, &#039;param&#039;, &#039;script&#039;, &#039;style&#039;]): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tags` | **mixed** |  |





***

### encode_instead_of_strip



```php
public encode_instead_of_strip(mixed $encode = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encode` | **mixed** |  |





***

### rename_attributes



```php
public rename_attributes(mixed $attribs = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### strip_attributes



```php
public strip_attributes(mixed $attribs = [&#039;bgsound&#039;, &#039;expr&#039;, &#039;id&#039;, &#039;style&#039;, &#039;onclick&#039;, &#039;onerror&#039;, &#039;onfinish&#039;, &#039;onmouseover&#039;, &#039;onmouseout&#039;, &#039;onfocus&#039;, &#039;onblur&#039;, &#039;lowsrc&#039;, &#039;dynsrc&#039;]): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### add_attributes



```php
public add_attributes(mixed $attribs = [&#039;audio&#039; =&gt; [&#039;preload&#039; =&gt; &#039;none&#039;], &#039;iframe&#039; =&gt; [&#039;sandbox&#039; =&gt; &#039;allow-scripts allow-same-origin&#039;], &#039;video&#039; =&gt; [&#039;preload&#039; =&gt; &#039;none&#039;]]): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





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

### set_output_encoding



```php
public set_output_encoding(mixed $encoding = &#039;UTF-8&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **mixed** |  |





***

### set_url_replacements

Set element/attribute key/value pairs of HTML attributes
containing URLs that need to be resolved relative to the feed

```php
public set_url_replacements(array|null $element_attribute = null): mixed
```

Defaults to |a|@href, |area|@href, |audio|@src, |blockquote|@cite,
|del|@cite, |form|@action, |img|@longdesc, |img|@src, |input|@src,
|ins|@cite, |q|@cite, |source|@src, |video|@src






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element_attribute` | **array&#124;null** | Element/attribute key/value pairs, null for default |





***

### set_https_domains

Set the list of domains for which to force HTTPS.

```php
public set_https_domains(mixed $domains): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$domains` | **mixed** |  |





**See Also:**

* \SimplePie\Misc::https_url() - Example array('biz', 'example.com', 'example.org', 'www.example.net');

***

### is_https_domain

Check if the domain is in the list of forced HTTPS.

```php
protected is_https_domain(mixed $domain): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$domain` | **mixed** |  |





***

### https_url

Force HTTPS for selected Web sites.

```php
public https_url(mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### sanitize



```php
public sanitize(mixed $data, mixed $type, mixed $base = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$type` | **mixed** |  |
| `$base` | **mixed** |  |





***

### preprocess



```php
protected preprocess(mixed $html, mixed $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **mixed** |  |
| `$type` | **mixed** |  |





***

### replace_urls



```php
public replace_urls(mixed $document, mixed $tag, mixed $attributes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$document` | **mixed** |  |
| `$tag` | **mixed** |  |
| `$attributes` | **mixed** |  |





***

### do_strip_htmltags



```php
public do_strip_htmltags(mixed $match): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$match` | **mixed** |  |





***

### strip_tag



```php
protected strip_tag(mixed $tag, mixed $document, mixed $xpath, mixed $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **mixed** |  |
| `$document` | **mixed** |  |
| `$xpath` | **mixed** |  |
| `$type` | **mixed** |  |





***

### strip_attr



```php
protected strip_attr(mixed $attrib, mixed $xpath): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attrib` | **mixed** |  |
| `$xpath` | **mixed** |  |





***

### rename_attr



```php
protected rename_attr(mixed $attrib, mixed $xpath): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attrib` | **mixed** |  |
| `$xpath` | **mixed** |  |





***

### add_attr



```php
protected add_attr(mixed $tag, mixed $valuePairs, mixed $document): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **mixed** |  |
| `$valuePairs` | **mixed** |  |
| `$document` | **mixed** |  |





***

### get_cache

Get a DataCache

```php
private get_cache(string $image_url = &#039;&#039;): \SimplePie\Cache\DataCache
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image_url` | **string** | Only needed for BC, can be removed in SimplePie 2.0.0 |





***


***
> Automatically generated on 2025-03-15
