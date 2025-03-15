
# Misc

Miscellaneous utilities



* Full name: `\SimplePie\Misc`



## Properties


### SIMPLEPIE_BUILD



```php
private static $SIMPLEPIE_BUILD
```



* This property is **static**.


***

## Methods


### time_hms



```php
public static time_hms(mixed $seconds): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$seconds` | **mixed** |  |





***

### absolutize_url



```php
public static absolutize_url(mixed $relative, mixed $base): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$relative` | **mixed** |  |
| `$base` | **mixed** |  |





***

### get_element

Get a HTML/XML element from a HTML string

```php
public static get_element(string $realname, string $string): array
```



* This method is **static**.


* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realname` | **string** | Element name (including namespace prefix if applicable) |
| `$string` | **string** | HTML document |





***

### element_implode



```php
public static element_implode(mixed $element): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** |  |





***

### error



```php
public static error(mixed $message, mixed $level, mixed $file, mixed $line): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **mixed** |  |
| `$level` | **mixed** |  |
| `$file` | **mixed** |  |
| `$line` | **mixed** |  |





***

### fix_protocol



```php
public static fix_protocol(mixed $url, mixed $http = 1): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$http` | **mixed** |  |





***

### array_merge_recursive



```php
public static array_merge_recursive(mixed $array1, mixed $array2): mixed
```



* This method is **static**.


* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array1` | **mixed** |  |
| `$array2` | **mixed** |  |





***

### parse_url



```php
public static parse_url(mixed $url): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### compress_parse_url



```php
public static compress_parse_url(mixed $scheme = &#039;&#039;, mixed $authority = &#039;&#039;, mixed $path = &#039;&#039;, mixed $query = &#039;&#039;, mixed $fragment = &#039;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scheme` | **mixed** |  |
| `$authority` | **mixed** |  |
| `$path` | **mixed** |  |
| `$query` | **mixed** |  |
| `$fragment` | **mixed** |  |





***

### normalize_url



```php
public static normalize_url(mixed $url): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### percent_encoding_normalization



```php
public static percent_encoding_normalization(mixed $match): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$match` | **mixed** |  |





***

### windows_1252_to_utf8

Converts a Windows-1252 encoded string to a UTF-8 encoded string

```php
public static windows_1252_to_utf8(string $string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | Windows-1252 encoded string |


**Return Value:**

UTF-8 encoded string




***

### change_encoding

Change a string from one encoding to another

```php
public static change_encoding(string $data, string $input, string $output): string|bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Raw data in $input encoding |
| `$input` | **string** | Encoding of $data |
| `$output` | **string** | Encoding you want |


**Return Value:**

False if we can't convert it




***

### change_encoding_mbstring



```php
protected static change_encoding_mbstring(mixed $data, mixed $input, mixed $output): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$input` | **mixed** |  |
| `$output` | **mixed** |  |





***

### change_encoding_iconv



```php
protected static change_encoding_iconv(mixed $data, mixed $input, mixed $output): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$input` | **mixed** |  |
| `$output` | **mixed** |  |





***

### change_encoding_uconverter



```php
protected static change_encoding_uconverter(string $data, string $input, string $output): string|false
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |
| `$input` | **string** |  |
| `$output` | **string** |  |





***

### encoding

Normalize an encoding name

```php
public static encoding(string $charset): string
```

This is automatically generated by create.php

To generate it, run `php create.php` on the command line, and copy the
output to replace this function.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$charset` | **string** | Character set to standardise |


**Return Value:**

Standardised name




***

### get_curl_version



```php
public static get_curl_version(): mixed
```



* This method is **static**.








***

### strip_comments

Strip HTML comments

```php
public static strip_comments(string $data): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Data to strip comments from |


**Return Value:**

Comment stripped string




***

### parse_date



```php
public static parse_date(mixed $dt): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dt` | **mixed** |  |





***

### entities_decode

Decode HTML entities

```php
public static entities_decode(string $data): string
```



* This method is **static**.


* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Input data |


**Return Value:**

Output data




***

### uncomment_rfc822

Remove RFC822 comments

```php
public static uncomment_rfc822(mixed $string): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |


**Return Value:**

Comment stripped string




***

### parse_mime



```php
public static parse_mime(mixed $mime): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mime` | **mixed** |  |





***

### atom_03_construct_type



```php
public static atom_03_construct_type(mixed $attribs): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### atom_10_construct_type



```php
public static atom_10_construct_type(mixed $attribs): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### atom_10_content_construct_type



```php
public static atom_10_content_construct_type(mixed $attribs): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attribs` | **mixed** |  |





***

### is_isegment_nz_nc



```php
public static is_isegment_nz_nc(mixed $string): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### space_separated_tokens



```php
public static space_separated_tokens(mixed $string): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### codepoint_to_utf8

Converts a unicode codepoint to a UTF-8 character

```php
public static codepoint_to_utf8(int $codepoint): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$codepoint` | **int** | Unicode codepoint |


**Return Value:**

UTF-8 character




***

### parse_str

Similar to parse_str()

```php
public static parse_str(string $str): array
```

Returns an associative array of name/value pairs, where the value is an
array of values that have used the same name

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | The input string. |





***

### xml_encoding

Detect XML encoding, as per XML 1.0 Appendix F.1

```php
public static xml_encoding(string $data, \SimplePie\Registry $registry): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | XML data |
| `$registry` | **\SimplePie\Registry** | Class registry |


**Return Value:**

Possible encodings




***

### output_javascript



```php
public static output_javascript(): mixed
```



* This method is **static**.








***

### get_build

Get the SimplePie build timestamp

```php
public static get_build(): mixed
```

Uses the git index if it exists, otherwise uses the modification time
of the newest file.

* This method is **static**.








***

### get_default_useragent

Get the default user agent string

```php
public static get_default_useragent(): string
```



* This method is **static**.








***

### debug

Format debugging information

```php
public static debug(mixed& $sp): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sp` | **mixed** |  |





***

### silence_errors



```php
public static silence_errors(mixed $num, mixed $str): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$num` | **mixed** |  |
| `$str` | **mixed** |  |





***

### url_remove_credentials

Sanitize a URL by removing HTTP credentials.

```php
public static url_remove_credentials(string $url): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** | the URL to sanitize. |


**Return Value:**

the same URL without HTTP credentials.




***


***
> Automatically generated on 2025-03-15
