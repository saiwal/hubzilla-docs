
# idna_convert

Encode/decode Internationalized Domain Names.

The class allows to convert internationalized domain names
(see RFC 3490 for details) as they can be used with various registries worldwide
to be translated between their original (localized) form and their encoded form
as it will be used in the DNS (Domain Name System).

The class provides two public methods, encode() and decode(), which do exactly
what you would expect them to do. You are allowed to use complete domain names,
simple strings and complete email addresses as well. That means, that you might
use any of the following notations:

- www.nörgler.com
- xn--nrgler-wxa
- xn--brse-5qa.xn--knrz-1ra.info

Unicode input might be given as either UTF-8 string, UCS-4 string or UCS-4
array. Unicode output is available in the same formats.
You can select your preferred format via {@link set_paramter()}.

ACE input and output is always expected to be ASCII.

* Full name: `\idna_convert`



## Properties


### NP

Holds all relevant mapping tables, loaded from a seperate file on construct
See RFC3454 for details

```php
public array $NP
```






***

### _punycode_prefix



```php
public $_punycode_prefix
```






***

### _invalid_ucs



```php
public $_invalid_ucs
```






***

### _max_ucs



```php
public $_max_ucs
```






***

### _base



```php
public $_base
```






***

### _tmin



```php
public $_tmin
```






***

### _tmax



```php
public $_tmax
```






***

### _skew



```php
public $_skew
```






***

### _damp



```php
public $_damp
```






***

### _initial_bias



```php
public $_initial_bias
```






***

### _initial_n



```php
public $_initial_n
```






***

### _sbase



```php
public $_sbase
```






***

### _lbase



```php
public $_lbase
```






***

### _vbase



```php
public $_vbase
```






***

### _tbase



```php
public $_tbase
```






***

### _lcount



```php
public $_lcount
```






***

### _vcount



```php
public $_vcount
```






***

### _tcount



```php
public $_tcount
```






***

### _ncount



```php
public $_ncount
```






***

### _scount



```php
public $_scount
```






***

### _error



```php
public $_error
```






***

### _api_encoding



```php
public $_api_encoding
```






***

### _allow_overlong



```php
public $_allow_overlong
```






***

### _strict_mode



```php
public $_strict_mode
```






***

## Methods


### __construct



```php
public __construct(mixed $options = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **mixed** |  |





***

### set_parameter

Sets a new option value. Available options and values:
[encoding - Use either UTF-8, UCS4 as array or UCS4 as string as input ('utf8' for UTF-8,
        'ucs4_string' and 'ucs4_array' respectively for UCS4); The output is always UTF-8]
[overlong - Unicode does not allow unnecessarily long encodings of chars,
            to allow this, set this parameter to true, else to false;
            default is false.]
[strict - true: strict mode, good for registration purposes - Causes errors
          on failures; false: loose mode, ideal for "wildlife" applications
          by silently ignoring errors and returning the original input instead

```php
public set_parameter(mixed $option, mixed $value = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$option` | **mixed** |  |
| `$value` | **mixed** |  |


**Return Value:**

true on success, false otherwise




***

### decode

Decode a given ACE domain name

```php
public decode(mixed $input, mixed $one_time_encoding = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$one_time_encoding` | **mixed** |  |


**Return Value:**

Decoded Domain name (UTF-8 or UCS-4)




***

### encode

Encode a given UTF-8 domain name

```php
public encode(mixed $decoded, mixed $one_time_encoding = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$decoded` | **mixed** |  |
| `$one_time_encoding` | **mixed** |  |


**Return Value:**

Encoded Domain name (ACE string)




***

### get_last_error

Use this method to get the last error ocurred

```php
public get_last_error(): string
```









**Return Value:**

The last error, that occured




***

### _decode

The actual decoding algorithm

```php
public _decode(mixed $encoded): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoded` | **mixed** |  |





***

### _encode

The actual encoding algorithm

```php
public _encode(mixed $decoded): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$decoded` | **mixed** |  |





***

### _adapt

Adapt the bias according to the current code point and position

```php
public _adapt(mixed $delta, mixed $npoints, mixed $is_first): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$delta` | **mixed** |  |
| `$npoints` | **mixed** |  |
| `$is_first` | **mixed** |  |





***

### _encode_digit

Encoding a certain digit

```php
public _encode_digit(mixed $d): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$d` | **mixed** |  |





***

### _decode_digit

Decode a certain digit

```php
public _decode_digit(mixed $cp): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cp` | **mixed** |  |





***

### _error

Internal error handling method

```php
public _error(mixed $error = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error` | **mixed** |  |





***

### _nameprep

Do Nameprep according to RFC3491 and RFC3454

```php
public _nameprep(mixed $input): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |


**Return Value:**

Unicode Characters, Nameprep'd




***

### _hangul_decompose

Decomposes a Hangul syllable
(see http://www.unicode.org/unicode/reports/tr15/#Hangul

```php
public _hangul_decompose(mixed $char): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$char` | **mixed** |  |


**Return Value:**

Either Hangul Syllable decomposed or original 32bit value as one value array




***

### _hangul_compose

Ccomposes a Hangul syllable
(see http://www.unicode.org/unicode/reports/tr15/#Hangul

```php
public _hangul_compose(mixed $input): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |


**Return Value:**

UCS4 sequence with syllables composed




***

### _get_combining_class

Returns the combining class of a certain wide char

```php
public _get_combining_class(mixed $char): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$char` | **mixed** |  |


**Return Value:**

Combining class if found, else 0




***

### _apply_cannonical_ordering

Apllies the cannonical ordering of a decomposed UCS4 sequence

```php
public _apply_cannonical_ordering(mixed $input): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |


**Return Value:**

Ordered USC4 sequence




***

### _combine

Do composition of a sequence of starter and non-starter

```php
public _combine(mixed $input): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |


**Return Value:**

Ordered USC4 sequence




***

### _utf8_to_ucs4

This converts an UTF-8 encoded string to its UCS-4 representation
By talking about UCS-4 "strings" we mean arrays of 32bit integers representing
each of the "chars". This is due to PHP not being able to handle strings with
bit depth different from 8. This apllies to the reverse method _ucs4_to_utf8(), too.

```php
public _utf8_to_ucs4(mixed $input): mixed
```

The following UTF-8 encodings are supported:
bytes bits  representation
1        7  0xxxxxxx
2       11  110xxxxx 10xxxxxx
3       16  1110xxxx 10xxxxxx 10xxxxxx
4       21  11110xxx 10xxxxxx 10xxxxxx 10xxxxxx
5       26  111110xx 10xxxxxx 10xxxxxx 10xxxxxx 10xxxxxx
6       31  1111110x 10xxxxxx 10xxxxxx 10xxxxxx 10xxxxxx 10xxxxxx
Each x represents a bit that can be used to store character data.
The five and six byte sequences are part of Annex D of ISO/IEC 10646-1:2000






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***

### _ucs4_to_utf8

Convert UCS-4 string into UTF-8 string
See _utf8_to_ucs4() for details

```php
public _ucs4_to_utf8(mixed $input): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***

### _ucs4_to_ucs4_string

Convert UCS-4 array into UCS-4 string

```php
public _ucs4_to_ucs4_string(mixed $input): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***

### _ucs4_string_to_ucs4

Convert UCS-4 strin into UCS-4 garray

```php
public _ucs4_string_to_ucs4(mixed $input): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
