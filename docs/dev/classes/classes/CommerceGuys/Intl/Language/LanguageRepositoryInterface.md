***

# LanguageRepositoryInterface

Language repository interface.



* Full name: `\CommerceGuys\Intl\Language\LanguageRepositoryInterface`



## Methods


### get

Gets a language matching the provided language code.

```php
public get(string $languageCode, string $locale = null): \CommerceGuys\Intl\Language\Language
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$languageCode` | **string** | The language code. |
| `$locale` | **string** | The locale (i.e. fr-FR). |





***

### getAll

Gets all languages.

```php
public getAll(string $locale = null): \CommerceGuys\Intl\Language\Language[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale (i.e. fr-FR). |


**Return Value:**

An array of languages, keyed by language code.




***

### getList

Gets a list of languages.

```php
public getList(string $locale = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale (i.e. fr-FR). |


**Return Value:**

An array of language names, keyed by language code.




***


***
> Automatically generated on 2025-03-15
