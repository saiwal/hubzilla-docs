***

# URLify

A fast PHP slug generator and transliteration library, started as a PHP port of URLify.js
from the Django project + fallback via "Portable ASCII".

- https://github.com/django/django/blob/master/django/contrib/admin/static/admin/js/urlify.js
- https://github.com/voku/portable-ascii

Handles symbols from latin languages, Arabic, Azerbaijani, Bulgarian, Burmese, Croatian, Czech, Danish, Esperanto,
Estonian, Finnish, French, Switzerland (French), Austrian (French), Georgian, German, Switzerland (German),
Austrian (German), Greek, Hindi, Kazakh, Latvian, Lithuanian, Norwegian, Persian, Polish, Romanian, Russian, Swedish,
Serbian, Slovak, Turkish, Ukrainian and Vietnamese ... and many other via "ASCII::to_transliterate()".

* Full name: `\URLify`



## Properties


### maps

The language-mapping array.

```php
public static array[] $maps
```

ISO 639-1 codes: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes

* This property is **static**.


***

### remove_list

List of words to remove from URLs.

```php
public static array[] $remove_list
```



* This property is **static**.


***

### arrayToSeparator

An array of strings that will convert into the separator-char - used by "URLify::filter()".

```php
private static string[] $arrayToSeparator
```



* This property is **static**.


***

## Methods


### add_array_to_separator

Add new strings the will be replaced with the separator.

```php
public static add_array_to_separator(array $array, bool $merge = true): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** | &lt;p&gt;An array of things that should replaced by the separator.&lt;/p&gt; |
| `$merge` | **bool** | &lt;p&gt;Keep the previous (default) array-to-separator array.&lt;/p&gt; |





***

### add_chars

Add new characters to the list. `$map` should be a hash.

```php
public static add_chars(array $map, string|null $language = null): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map` | **array** |  |
| `$language` | **string&#124;null** |  |





***

### reset_chars



```php
public static reset_chars(): void
```



* This method is **static**.








***

### downcode

Transliterates characters to their ASCII equivalents.

```php
public static downcode(string $string, string $language = &#039;en&#039;, string $unknown = &#039;&#039;): string
```

$language specifies a priority for a specific language.
The latter is useful if languages have different rules for the same character.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | &lt;p&gt;The input string.&lt;/p&gt; |
| `$language` | **string** | &lt;p&gt;Your primary language.&lt;/p&gt; |
| `$unknown` | **string** | &lt;p&gt;Character use if character unknown. (default is ?).&lt;/p&gt; |





***

### slug

Convert a String to URL slug. Wraps <strong>filter()</strong> with a simpler
set of defaults for typical usage in generating blog post slugs.

```php
public static slug(string $string, int $maxLength = 200, string $separator = &#039;-&#039;, string $language = &#039;en&#039;): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | &lt;p&gt;The text you want to convert.&lt;/p&gt; |
| `$maxLength` | **int** | &lt;p&gt;Max. length of the output string, set to &quot;0&quot; (zero) to<br />disable it&lt;/p&gt; |
| `$separator` | **string** | &lt;p&gt;Define a new separator for the words.&lt;/p&gt; |
| `$language` | **string** | &lt;p&gt;The language you want to convert to.&lt;/p&gt; |





***

### filter

Convert a String to URL.

```php
public static filter(string $string, int $maxLength = 200, string $language = &#039;en&#039;, bool $fileName = false, bool $removeWords = false, bool $strToLower = true, bool|string $separator = &#039;-&#039;): string
```

e.g.: "Petty<br>theft" to "Petty-theft"

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | &lt;p&gt;The text you want to convert.&lt;/p&gt; |
| `$maxLength` | **int** | &lt;p&gt;Max. length of the output string, set to &quot;0&quot; (zero) to<br />disable it&lt;/p&gt; |
| `$language` | **string** | &lt;p&gt;The language you want to convert to.&lt;/p&gt; |
| `$fileName` | **bool** | &lt;p&gt;<br />Keep the &quot;.&quot; from the extension e.g.: &quot;imaäe.jpg&quot; =&gt;<br />&quot;image.jpg&quot;<br />&lt;/p&gt; |
| `$removeWords` | **bool** | &lt;p&gt;<br />Remove some &quot;words&quot; from the string.&lt;br /&gt;<br />Info: Set extra words via &lt;strong&gt;remove_words()&lt;/strong&gt;.<br />&lt;/p&gt; |
| `$strToLower` | **bool** | &lt;p&gt;Use &lt;strong&gt;strtolower()&lt;/strong&gt; at the end.&lt;/p&gt; |
| `$separator` | **bool&#124;string** | &lt;p&gt;Define a new separator for the words.&lt;/p&gt; |





***

### remove_words

Append words to the remove list. Accepts either single words or an array of words.

```php
public static remove_words(string|string[] $words, string $language = &#039;en&#039;, bool $merge = true): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$words` | **string&#124;string[]** |  |
| `$language` | **string** |  |
| `$merge` | **bool** | &lt;p&gt;Keep the previous (default) remove-words array.&lt;/p&gt; |





***

### reset_array_to_separator

Reset the internal "self::$arrayToSeparator" to the default values.

```php
public static reset_array_to_separator(): void
```



* This method is **static**.








***

### reset_remove_list

reset the word-remove-array

```php
public static reset_remove_list(string $language = &#039;en&#039;): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$language` | **string** |  |





***

### transliterate

Alias of `URLify::downcode()`.

```php
public static transliterate(string $string, string $language = &#039;en&#039;): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$language` | **string** |  |





***

### expandString

Expands the given string replacing some special parts for words.

```php
protected static expandString(string $string, string $language = &#039;en&#039;): string
```

e.g. "lorem@ipsum.com" is replaced by "lorem at ipsum dot com".

Most of these transformations have been inspired by the pelle/slugger
project, distributed under the Eclipse Public License.
Copyright 2012 Pelle Braendgaard

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | The string to expand |
| `$language` | **string** |  |


**Return Value:**

The result of expanding the string




***

### get_language_for_reset_remove_list



```php
private static get_language_for_reset_remove_list(string $language): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$language` | **string** |  |





***

### expandCurrencies

Expands the numeric currencies in euros, dollars, pounds
and yens that the given string may include.

```php
private static expandCurrencies(string $string, string $language = &#039;en&#039;): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$language` | **string** |  |





***

### expandSymbols

Expands the special symbols that the given string may include, such as '@', '.', '#' and '%'.

```php
private static expandSymbols(string $string, string $language = &#039;en&#039;): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$language` | **string** |  |





***

### get_remove_list

return the "self::$remove_list[$language]" array

```php
private static get_remove_list(string $language = &#039;en&#039;): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$language` | **string** |  |





***


***
> Automatically generated on 2025-03-15
