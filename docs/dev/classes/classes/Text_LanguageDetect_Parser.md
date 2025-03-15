
# Text_LanguageDetect_Parser

This class represents a text sample to be parsed.

This separates the analysis of a text sample from the primary LanguageDetect
class. After a new profile has been built, the data can be retrieved using
the accessor functions.

This class is intended to be used by the Text_LanguageDetect class, not
end-users.

* Full name: `\Text_LanguageDetect_Parser`
* Parent class: [`\Text_LanguageDetect`](./Text_LanguageDetect.md)

**See Also:**

* http://pear.php.net/package/Text_LanguageDetect/ - 



## Properties


### _string

The piece of text being parsed

```php
protected string $_string
```






***

### _trigram

Stores the trigram frequencies of the sample

```php
protected string $_trigram
```






***

### _trigram_ranks

Stores the trigram ranks of the sample

```php
protected array $_trigram_ranks
```






***

### _unicode_blocks

Stores the unicode blocks of the sample

```php
protected array $_unicode_blocks
```






***

### _compile_unicode

Whether the parser should compile the unicode ranges

```php
protected bool $_compile_unicode
```






***

### _compile_trigram

Whether the parser should compile trigrams

```php
protected bool $_compile_trigram
```






***

### _trigram_pad_start

Whether the trigram parser should pad the beginning of the string

```php
protected bool $_trigram_pad_start
```






***

### _unicode_skip_symbols

Whether the unicode parser should skip non-alphabetical ascii chars

```php
protected bool $_unicode_skip_symbols
```






***

## Methods


### __construct

Constructor

```php
public __construct(string $string): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | string to be parsed |





***

### Text_LanguageDetect_Parser

PHP 4 constructor for backwards compatibility.

```php
public Text_LanguageDetect_Parser(string $string): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | string to be parsed |





***

### validateString

Returns true if a string is suitable for parsing

```php
public static validateString(string $str): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | input string to test |


**Return Value:**

true if acceptable, false if not




***

### prepareTrigram

Turn on/off trigram counting

```php
public prepareTrigram(bool $bool = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bool` | **bool** | true for on, false for off |





***

### prepareUnicode

Turn on/off unicode block counting

```php
public prepareUnicode(bool $bool = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bool` | **bool** | true for on, false for off |





***

### setPadStart

Turn on/off padding the beginning of the sample string

```php
public setPadStart(bool $bool = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bool` | **bool** | true for on, false for off |





***

### setUnicodeSkipSymbols

Should the unicode block counter skip non-alphabetical ascii chars?

```php
public setUnicodeSkipSymbols(bool $bool = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bool` | **bool** | true for on, false for off |





***

### getTrigramRanks

Returns the trigram ranks for the text sample

```php
public getTrigramRanks(): array
```









**Return Value:**

Trigram ranks in the text sample




***

### getTrigramFreqs

Return the trigram freqency table

```php
public getTrigramFreqs(): array
```

Only used in testing to make sure the parser is working







**Return Value:**

Trigram freqencies in the text sample




***

### getUnicodeBlocks

Returns the array of unicode blocks

```php
public getUnicodeBlocks(): array
```









**Return Value:**

Unicode blocks in the text sample




***

### analyze

Executes the parsing operation

```php
public analyze(): void
```

Be sure to call the set*() functions to set options and the
prepare*() functions first to tell it what kind of data to compute

Afterwards the get*() functions can be used to access the compiled
information.










***


## Inherited methods


### __construct

Constructor

```php
public __construct(): mixed
```

Will attempt to load the language database. If it fails, you will get
an exception.










***

### _get_data_loc

Returns the path to the location of the database

```php
protected _get_data_loc(string $fname): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fname` | **string** | File name to load |


**Return Value:**

expected path to the language model database




***

### _readdb

Loads the language trigram database from filename

```php
protected _readdb(string $fname): array
```

Trigram datbase should be a serialize()'d array






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fname` | **string** | the filename where the data is stored |


**Return Value:**

the language model data



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### _checkTrigram

Checks if this object is ready to detect languages

```php
protected _checkTrigram(array $trigram): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$trigram` | **array** | Trigram data from database |





***

### omitLanguages

Omits languages

```php
public omitLanguages(mixed $omit_list, bool $include_only = false): int
```

Pass this function the name of or an array of names of
languages that you don't want considered

If you're only expecting a limited set of languages, this can greatly
speed up processing






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$omit_list` | **mixed** | language name or array of names to omit |
| `$include_only` | **bool** | if true will include (rather than<br />exclude) only those in the list |


**Return Value:**

number of languages successfully deleted



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### getLanguageCount

Returns the number of languages that this object can detect

```php
public getLanguageCount(): int
```









**Return Value:**

the number of languages



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### languageExists

Checks if the language with the given name exists in the database

```php
public languageExists(mixed $lang): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang` | **mixed** | Language name or array of language names |


**Return Value:**

true if language model exists




***

### getLanguages

Returns the list of detectable languages

```php
public getLanguages(): array
```









**Return Value:**

the names of the languages known to this object<<<<<<<



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### setPerlCompatible

Make this object behave like Language::Guess

```php
public setPerlCompatible(bool $setting = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$setting` | **bool** | false to turn off perl compatibility |





***

### setNameMode

Sets the way how language names are accepted and returned.

```php
public setNameMode(int $name_mode): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name_mode` | **int** | One of the following modes:<br />0 - language name (&quot;english&quot;)<br />2 - 2-letter ISO 639-1 code (&quot;en&quot;)<br />3 - 3-letter ISO 639-2 code (&quot;eng&quot;) |





***

### useUnicodeBlocks

Whether to use unicode block ranges in detection

```php
public useUnicodeBlocks(bool $setting = true): void
```

Should speed up most detections if turned on (detault is on). In some
circumstances it may be slower, such as for large text samples (> 10K)
in languages that use latin scripts. In other cases it should speed up
detection noticeably.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$setting` | **bool** | false to turn off |





***

### _trigram

Converts a piece of text into trigrams

```php
protected _trigram(string $text): array
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** | text to convert |


**Return Value:**

array of trigram frequencies




***

### _arr_rank

Converts a set of trigrams from frequencies to ranks

```php
protected _arr_rank(array $arr): array
```

Thresholds (cuts off) the list at $this->_threshold






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | array of trigram |


**Return Value:**

ranks of trigrams




***

### _bub_sort

Sorts an array by value breaking ties alphabetically

```php
protected _bub_sort(array& $arr): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | the array to sort |





***

### _sort_func

Sort function used by bubble sort

```php
protected _sort_func(array $a, array $b): int
```

Callback function for usort().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **array** | first param passed by usort() |
| `$b` | **array** | second param passed by usort() |


**Return Value:**

1 if $a is greater, -1 if not




**See Also:**

* \_bub_sort() - 

***

### _distance

Calculates a linear rank-order distance statistic between two sets of
ranked trigrams

```php
protected _distance(array $arr1, array $arr2): int
```

Sums the differences in rank for each trigram. If the trigram does not
appear in both, consider it a difference of $this->_threshold.

This distance measure was proposed by Cavnar & Trenkle (1994). Despite
its simplicity it has been shown to be highly accurate for language
identification tasks.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr1` | **array** | the reference set of trigram ranks |
| `$arr2` | **array** | the target set of trigram ranks |


**Return Value:**

the sum of the differences between the ranks of
the two trigram sets




***

### _normalize_score

Normalizes the score returned by _distance()

```php
protected _normalize_score(int $score, int $base_count = null): float
```

Different if perl compatible or not






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$score` | **int** | the score from _distance() |
| `$base_count` | **int** | the number of trigrams being considered |


**Return Value:**

the normalized score




**See Also:**

* \_distance() - 

***

### detect

Detects the closeness of a sample of text to the known languages

```php
public detect(string $sample, int $limit): mixed
```

Calculates the statistical difference between the text and
the trigrams for each language, normalizes the score then
returns results for all languages in sorted order

If perl compatible, the score is 300-0, 0 being most similar.
Otherwise, it's 0-1 with 1 being most similar.

The $sample text should be at least a few sentences in length;
should be ascii-7 or utf8 encoded, if another and the mbstring extension
is present it will try to detect and convert. However, experience has
shown that mb_detect_encoding() *does not work very well* with at least
some types of encoding.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sample` | **string** | a sample of text to compare. |
| `$limit` | **int** | if specified, return an array of the most likely<br />$limit languages and their scores. |


**Return Value:**

sorted array of language scores, blank array if no
useable text was found



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



**See Also:**

* \_distance() - 

***

### detectSimple

Returns only the most similar language to the text sample

```php
public detectSimple(string $sample): string
```

Calls $this->detect() and returns only the top result






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sample` | **string** | text to detect the language of |


**Return Value:**

the name of the most likely language
or null if no language is similar



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



**See Also:**

* \detect() - 

***

### detectConfidence

Returns an array containing the most similar language and a confidence
rating

```php
public detectConfidence(string $sample): array
```

Confidence is a simple measure calculated from the similarity score
minus the similarity score from the next most similar language
divided by the highest possible score. Languages that have closely
related cousins (e.g. Norwegian and Danish) should generally have lower
confidence scores.

The similarity score answers the question "How likely is the text the
returned language regardless of the other languages considered?" The
confidence score is one way of answering the question "how likely is the
text the detected language relative to the rest of the language model
set?"

To see how similar languages are a priori, see languageSimilarity()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sample` | **string** | text for which language will be detected |


**Return Value:**

most similar language, score and confidence rating
or null if no language is similar



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



**See Also:**

* \detect() - 

***

### detectUnicodeBlocks

Returns the distribution of unicode blocks in a given utf8 string

```php
public detectUnicodeBlocks(string $str, bool $skip_symbols): array
```

For the block name of a single char, use unicodeBlockName()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | input string. Must be ascii or utf8 |
| `$skip_symbols` | **bool** | if true, skip ascii digits, symbols and<br />non-printing characters. Includes spaces,<br />newlines and common punctutation characters. |




**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### unicodeBlockName

Returns the block name for a given unicode value

```php
public unicodeBlockName(mixed $unicode): mixed
```

If passed a string, will assume it is being passed a UTF8-formatted
character and will automatically convert. Otherwise it will assume it
is being passed a numeric unicode value.

Make sure input is of the correct type!






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$unicode` | **mixed** | unicode value or utf8 char |


**Return Value:**

the block name string or false if not found



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### _unicode_block_name

Searches the unicode block database

```php
protected _unicode_block_name(int $unicode, array $blocks, int $block_count = -1): mixed
```

Returns the block name for a given unicode value. unicodeBlockName() is
the public interface for this function, which does input checks which
this function omits for speed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$unicode` | **int** | the unicode value |
| `$blocks` | **array** | the block database |
| `$block_count` | **int** | the number of defined blocks in the database |


**Return Value:**

Block name, -1 if it failed




**See Also:**

* \unicodeBlockName() - 

***

### _read_unicode_block_db

Brings up the unicode block database

```php
protected _read_unicode_block_db(): array
```









**Return Value:**

the database of unicode block definitions



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### languageSimilarity

Calculate the similarities between the language models

```php
public languageSimilarity(string $lang1 = null, string $lang2 = null): array
```

Use this function to see how similar languages are to each other.

If passed 2 language names, will return just those languages compared.
If passed 1 language name, will return that language compared to
all others.
If passed none, will return an array of every language model compared
to every other one.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang1` | **string** | the name of the first language to be compared |
| `$lang2` | **string** | the name of the second language to be compared |


**Return Value:**

scores of every language compared
or the score of just the provided languages
or null if one of the supplied languages does not exist



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



***

### clusterLanguages

Cluster known languages according to languageSimilarity()

```php
public clusterLanguages(): array
```

WARNING: this method is EXPERIMENTAL. It is not recommended for common
use, and it may disappear or its functionality may change in future
releases without notice.

Uses a nearest neighbor technique to generate the maximum possible
number of dendograms from the similarity data.




* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.




**Return Value:**

language cluster data



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



**See Also:**

* \languageSimilarity() - 

***

### clusteredSearch

Perform an intelligent detection based on clusterLanguages()

```php
public clusteredSearch(string $str): array
```

WARNING: this method is EXPERIMENTAL. It is not recommended for common
use, and it may disappear or its functionality may change in future
releases without notice.

This compares the sample text to top the top level of clusters. If the
sample is similar to the cluster it will drop down and compare it to the
languages in the cluster, and so on until it hits a leaf node.

this should find the language in considerably fewer compares
(the equivalent of a binary search), however clusterLanguages() is costly
and the loss of accuracy from this technique is significant.

This method may need to be 'fuzzier' in order to become more accurate.

This function could be more useful if the universe of possible languages
was very large, however in such cases some method of Bayesian inference
might be more helpful.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | input string |


**Return Value:**

language scores (only those compared)



**Throws:**

- [`Text_LanguageDetect_Exception`](./Text_LanguageDetect_Exception.md)



**See Also:**

* \clusterLanguages() - 

***

### utf8strlen

UTF8-safe strlen()

```php
public static utf8strlen(string $str): int
```

Returns the numbers of characters (not bytes) in a utf8 string

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | string to get the length of |


**Return Value:**

number of chars




***

### _utf8char2unicode

Returns the unicode value of a utf8 char

```php
protected _utf8char2unicode(string $char): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$char` | **string** | a utf8 (possibly multi-byte) char |


**Return Value:**

unicode value




**See Also:**

* http://en.wikipedia.org/wiki/UTF-8 - 

***

### _next_char

UTF8-safe fast character iterator

```php
protected static _next_char(string $str, int& $counter, bool $special_convert = false): \char
```

Will get the next character starting from $counter, which will then be
incremented. If a multi-byte char the bytes will be concatenated and
$counter will be incremeted by the number of bytes in the char.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | the string being iterated over |
| `$counter` | **int** | the iterator, will increment by reference |
| `$special_convert` | **bool** | whether to do special conversions |


**Return Value:**

the next (possibly multi-byte) char from $counter




***

### _convertFromNameMode

Converts an $language input parameter from the configured mode
to the language name that is used internally.

```php
protected _convertFromNameMode(string|array $lang, bool $convertKey = false): string|array
```

Works for strings and arrays.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang` | **string&#124;array** | A language description (&quot;english&quot;/&quot;en&quot;/&quot;eng&quot;) |
| `$convertKey` | **bool** | If $lang is an array, setting $key<br />converts the keys to the language name. |


**Return Value:**

Language name




***

### _convertToNameMode

Converts an $language output parameter from the language name that is
used internally to the configured mode.

```php
protected _convertToNameMode(string|array $lang, bool $convertKey = false): string|array
```

Works for strings and arrays.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang` | **string&#124;array** | A language description (&quot;english&quot;/&quot;en&quot;/&quot;eng&quot;) |
| `$convertKey` | **bool** | If $lang is an array, setting $key<br />converts the keys to the language name. |


**Return Value:**

Language name




***


***
> Automatically generated on 2025-03-15
