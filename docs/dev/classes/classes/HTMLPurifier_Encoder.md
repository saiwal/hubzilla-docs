
# HTMLPurifier_Encoder

A UTF-8 specific character encoder that handles cleaning and transforming.



* Full name: `\HTMLPurifier_Encoder`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`ICONV_OK`|public| |0|
|`ICONV_TRUNCATES`|public| |1|
|`ICONV_UNUSABLE`|public| |2|


## Methods


### __construct

Constructor throws fatal error if you attempt to instantiate class

```php
private __construct(): mixed
```












***

### muteErrorHandler

Error-handler that mutes errors, alternative to shut-up operator.

```php
public static muteErrorHandler(): mixed
```



* This method is **static**.








***

### unsafeIconv

iconv wrapper which mutes errors, but doesn't work around bugs.

```php
public static unsafeIconv(string $in, string $out, string $text): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **string** | Input encoding |
| `$out` | **string** | Output encoding |
| `$text` | **string** | The text to convert |





***

### iconv

iconv wrapper which mutes errors and works around bugs.

```php
public static iconv(string $in, string $out, string $text, int $max_chunk_size = 8000): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **string** | Input encoding |
| `$out` | **string** | Output encoding |
| `$text` | **string** | The text to convert |
| `$max_chunk_size` | **int** |  |





***

### cleanUTF8

Cleans a UTF-8 string for well-formedness and SGML validity

```php
public static cleanUTF8(string $str, bool $force_php = false): string
```

It will parse according to UTF-8 and return a valid UTF8 string, with
non-SGML codepoints excluded.

Specifically, it will permit:
\x{9}\x{A}\x{D}\x{20}-\x{7E}\x{A0}-\x{D7FF}\x{E000}-\x{FFFD}\x{10000}-\x{10FFFF}
Source: https://www.w3.org/TR/REC-xml/#NT-Char
Arguably this function should be modernized to the HTML5 set
of allowed characters:
https://www.w3.org/TR/html5/syntax.html#preprocessing-the-input-stream
which simultaneously expand and restrict the set of allowed characters.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | The string to clean |
| `$force_php` | **bool** |  |





***

### unichr

Translates a Unicode codepoint into its corresponding UTF-8 character.

```php
public static unichr(mixed $code): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **mixed** |  |





***

### iconvAvailable



```php
public static iconvAvailable(): bool
```



* This method is **static**.








***

### convertToUTF8

Convert a string to UTF-8 based on configuration.

```php
public static convertToUTF8(string $str, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | The string to convert |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### convertFromUTF8

Converts a string from UTF-8 based on configuration.

```php
public static convertFromUTF8(string $str, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | The string to convert |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### convertToASCIIDumbLossless

Lossless (character-wise) conversion of HTML to ASCII

```php
public static convertToASCIIDumbLossless(string $str): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | UTF-8 string to be converted to ASCII |


**Return Value:**

ASCII encoded string with non-ASCII character entity-ized




***

### testIconvTruncateBug

glibc iconv has a known bug where it doesn't handle the magic
//IGNORE stanza correctly.  In particular, rather than ignore
characters, it will return an EILSEQ after consuming some number
of characters, and expect you to restart iconv as if it were
an E2BIG.  Old versions of PHP did not respect the errno, and
returned the fragment, so as a result you would see iconv
mysteriously truncating output. We can work around this by
manually chopping our input into segments of about 8000
characters, as long as PHP ignores the error code.  If PHP starts
paying attention to the error code, iconv becomes unusable.

```php
public static testIconvTruncateBug(): int
```



* This method is **static**.





**Return Value:**

Error code indicating severity of bug.




***

### testEncodingSupportsASCII

This expensive function tests whether or not a given character
encoding supports ASCII. 7/8-bit encodings like Shift_JIS will
fail this test, and require special processing. Variable width
encodings shouldn't ever fail.

```php
public static testEncodingSupportsASCII(string $encoding, bool $bypass = false): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **string** | Encoding name to test, as per iconv format |
| `$bypass` | **bool** | Whether or not to bypass the precompiled arrays. |


**Return Value:**

of UTF-8 characters to their corresponding ASCII,
which can be used to "undo" any overzealous iconv action.




***


***
> Automatically generated on 2025-03-15
