
# LanguageRepository

Manages languages based on JSON definitions.



* Full name: `\CommerceGuys\Intl\Language\LanguageRepository`
* This class implements:
[`\CommerceGuys\Intl\Language\LanguageRepositoryInterface`](./LanguageRepositoryInterface.md)



## Properties


### defaultLocale

The default locale.

```php
protected string $defaultLocale
```






***

### fallbackLocale

The fallback locale.

```php
protected string $fallbackLocale
```






***

### definitionPath

The path where per-locale definitions are stored.

```php
protected string $definitionPath
```






***

### definitions

Per-locale language definitions.

```php
protected array $definitions
```






***

### availableLocales

The available locales.

```php
protected array $availableLocales
```






***

## Methods


### __construct

Creates a LanguageRepository instance.

```php
public __construct(string $defaultLocale = &#039;en&#039;, string $fallbackLocale = &#039;en&#039;, string $definitionPath = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$defaultLocale` | **string** | The default locale. Defaults to &#039;en&#039;. |
| `$fallbackLocale` | **string** | The fallback locale. Defaults to &#039;en&#039;. |
| `$definitionPath` | **string** | The path to the currency definitions.<br />Defaults to &#039;resources/language&#039;. |





***

### get

Gets a language matching the provided language code.

```php
public get(mixed $languageCode, mixed $locale = null): \CommerceGuys\Intl\Language\Language
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$languageCode` | **mixed** | The language code. |
| `$locale` | **mixed** | The locale (i.e. fr-FR). |





***

### getAll

Gets all languages.

```php
public getAll(mixed $locale = null): \CommerceGuys\Intl\Language\Language[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **mixed** | The locale (i.e. fr-FR). |


**Return Value:**

An array of languages, keyed by language code.




***

### getList

Gets a list of languages.

```php
public getList(mixed $locale = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **mixed** | The locale (i.e. fr-FR). |


**Return Value:**

An array of language names, keyed by language code.




***

### loadDefinitions

Loads the language definitions for the provided locale.

```php
protected loadDefinitions(string $locale): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The desired locale. |





***


***
> Automatically generated on 2025-03-18
