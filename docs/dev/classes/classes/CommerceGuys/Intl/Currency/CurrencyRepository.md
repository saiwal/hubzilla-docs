***

# CurrencyRepository

Manages currencies based on JSON definitions.



* Full name: `\CommerceGuys\Intl\Currency\CurrencyRepository`
* This class implements:
[`\CommerceGuys\Intl\Currency\CurrencyRepositoryInterface`](./CurrencyRepositoryInterface.md)



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

Per-locale currency definitions.

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

Creates a CurrencyRepository instance.

```php
public __construct(string $defaultLocale = &#039;en&#039;, string $fallbackLocale = &#039;en&#039;, string $definitionPath = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$defaultLocale` | **string** | The default locale. Defaults to &#039;en&#039;. |
| `$fallbackLocale` | **string** | The fallback locale. Defaults to &#039;en&#039;. |
| `$definitionPath` | **string** | The path to the currency definitions.<br />Defaults to &#039;resources/currency&#039;. |





***

### get

Gets a currency matching the provided currency code.

```php
public get(mixed $currencyCode, mixed $locale = null): \CommerceGuys\Intl\Currency\Currency
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$currencyCode` | **mixed** | The currency code. |
| `$locale` | **mixed** | The locale (i.e. fr-FR). |





***

### getAll

Gets all currencies.

```php
public getAll(mixed $locale = null): \CommerceGuys\Intl\Currency\Currency[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **mixed** | The locale (i.e. fr-FR). |


**Return Value:**

An array of currencies, keyed by currency code.




***

### getList

Gets a list of currencies.

```php
public getList(mixed $locale = null): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **mixed** | The locale (i.e. fr-FR). |


**Return Value:**

An array of currency names, keyed by currency code.




***

### loadDefinitions

Loads the currency definitions for the provided locale.

```php
protected loadDefinitions(string $locale): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The desired locale. |





***

### getBaseDefinitions

Gets the base currency definitions.

```php
protected getBaseDefinitions(): array
```

Contains data common to all locales: numeric code, fraction digits.







**Return Value:**


An array of definitions, keyed by currency code.
Each definition is a numerically indexed array containing:
- The numeric code.
- The fraction digits.




***


***
> Automatically generated on 2025-03-15
