***

# Locale





* Full name: `\CommerceGuys\Intl\Locale`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### aliases

Locale aliases.

```php
protected static array $aliases
```



* This property is **static**.


***

### parents

Locale parents.

```php
protected static array $parents
```



* This property is **static**.


***

## Methods


### match

Checks whether two locales match.

```php
public static match(string $firstLocale, string $secondLocale): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$firstLocale` | **string** | The first locale. |
| `$secondLocale` | **string** | The second locale. |


**Return Value:**

TRUE if the locales match, FALSE otherwise.




***

### matchCandidates

Checks whether two locales have at least one common candidate.

```php
public static matchCandidates(string $firstLocale, string $secondLocale): bool
```

For example, "de" and "de-AT" will match because they both have
"de" in common. This is useful for partial locale matching.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$firstLocale` | **string** | The first locale. |
| `$secondLocale` | **string** | The second locale. |


**Return Value:**

TRUE if there is a common candidate, FALSE otherwise.




**See Also:**

* \CommerceGuys\Intl\self::getCandidates - 

***

### resolve

Resolves the locale from the available locales.

```php
public static resolve(array $availableLocales, string $locale, string $fallbackLocale = null): string
```

Takes all locale candidates for the requested locale
and fallback locale, searches for them in the available
locale list. The first found locale is returned.
If no candidate is found in the list, an exception is thrown.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$availableLocales` | **array** | The available locales. |
| `$locale` | **string** | The requested locale (i.e. fr-FR). |
| `$fallbackLocale` | **string** | A fallback locale (i.e &quot;en&quot;). |




**Throws:**

- [`UnknownLocaleException`](./Exception/UnknownLocaleException.md)



**See Also:**

* \CommerceGuys\Intl\self::getCandidates - 

***

### canonicalize

Canonicalizes the given locale.

```php
public static canonicalize(string $locale): string
```

Standardizes separators and capitalization, turning
a locale such as "sr_rs_latn" into "sr-RS-Latn".

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale. |


**Return Value:**

The canonicalized locale.




***

### getCandidates

Gets locale candidates.

```php
public static getCandidates(string $locale, string $fallbackLocale = null): array
```

For example, "bs-Cyrl-BA" has the following candidates:
1) bs-Cyrl-BA
2) bs-Cyrl
3) bs

The locale is de-aliased, e.g. the candidates for "sh" are:
1) sr-Latn
2) sr

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale (i.e. fr-FR). |
| `$fallbackLocale` | **string** | A fallback locale (i.e &quot;en&quot;). |


**Return Value:**

An array of all variants of a locale.




***

### getParent

Gets the parent for the given locale.

```php
public static getParent(string $locale): string|null
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | <br />The locale. |


**Return Value:**


The parent, or null if none found.




***

### replaceAlias

Replaces a locale alias with the real locale.

```php
public static replaceAlias(string $locale): string
```

For example, "zh-CN" is replaced with "zh-Hans-CN".

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale. |


**Return Value:**

The locale.




***


***
> Automatically generated on 2025-03-15
