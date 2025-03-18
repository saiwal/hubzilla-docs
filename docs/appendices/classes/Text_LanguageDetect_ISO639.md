
# Text_LanguageDetect_ISO639

Provides a mapping between the languages from lang.dat and the
ISO 639-1 and ISO-639-2 codes.

Note that this class contains only languages that exist in lang.dat.

* Full name: `\Text_LanguageDetect_ISO639`

**See Also:**

* http://www.loc.gov/standards/iso639-2/php/code_list.php - 



## Properties


### nameToCode2

Maps all language names from the language database to the
ISO 639-1 2-letter language code.

```php
public static array $nameToCode2
```

NULL indicates that there is no 2-letter code.

* This property is **static**.


***

### nameToCode3

Maps all language names from the language database to the
ISO 639-2 3-letter language code.

```php
public static array $nameToCode3
```



* This property is **static**.


***

### code2ToName

Maps ISO 639-1 2-letter language codes to the language names
in the language database

```php
public static array $code2ToName
```

Not all languages have a 2 letter code, so some are missing

* This property is **static**.


***

### code3ToName

Maps ISO 639-2 3-letter language codes to the language names
in the language database.

```php
public static array $code3ToName
```



* This property is **static**.


***

## Methods


### nameToCode2

Returns the 2-letter ISO 639-1 code for the given language name.

```php
public static nameToCode2(string $lang): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang` | **string** | English language name like &quot;swedish&quot; |


**Return Value:**

Two-letter language code (e.g. "sv") or NULL if not found




***

### nameToCode3

Returns the 3-letter ISO 639-2 code for the given language name.

```php
public static nameToCode3(string $lang): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang` | **string** | English language name like &quot;swedish&quot; |


**Return Value:**

Three-letter language code (e.g. "swe") or NULL if not found




***

### code2ToName

Returns the language name for the given 2-letter ISO 639-1 code.

```php
public static code2ToName(string $code): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | Two-letter language code (e.g. &quot;sv&quot;) |


**Return Value:**

English language name like "swedish"




***

### code3ToName

Returns the language name for the given 3-letter ISO 639-2 code.

```php
public static code3ToName(string $code): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** | Three-letter language code (e.g. &quot;swe&quot;) |


**Return Value:**

English language name like "swedish"




***


***
> Automatically generated on 2025-03-18
