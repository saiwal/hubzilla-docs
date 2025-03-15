
# CurrencyRepositoryInterface

Currency repository interface.



* Full name: `\CommerceGuys\Intl\Currency\CurrencyRepositoryInterface`



## Methods


### get

Gets a currency matching the provided currency code.

```php
public get(string $currencyCode, string $locale = null): \CommerceGuys\Intl\Currency\Currency
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$currencyCode` | **string** | The currency code. |
| `$locale` | **string** | The locale (i.e. fr-FR). |





***

### getAll

Gets all currencies.

```php
public getAll(string $locale = null): \CommerceGuys\Intl\Currency\Currency[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale (i.e. fr-FR). |


**Return Value:**

An array of currencies, keyed by currency code.




***

### getList

Gets a list of currencies.

```php
public getList(string $locale = null): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale (i.e. fr-FR). |


**Return Value:**

An array of currency names, keyed by currency code.




***


***
> Automatically generated on 2025-03-15
