***

# NumberFormatRepository

Provides number formats.



* Full name: `\CommerceGuys\Intl\NumberFormat\NumberFormatRepository`
* This class implements:
[`\CommerceGuys\Intl\NumberFormat\NumberFormatRepositoryInterface`](./NumberFormatRepositoryInterface.md)



## Properties


### fallbackLocale

The fallback locale.

```php
protected string $fallbackLocale
```






***

## Methods


### __construct

Creates a NumberFormatRepository instance.

```php
public __construct(string $fallbackLocale = &#039;en&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fallbackLocale` | **string** | The fallback locale. Defaults to &#039;en&#039;. |





***

### get

Gets a number format for the provided locale.

```php
public get(mixed $locale): \CommerceGuys\Intl\NumberFormat\NumberFormat
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **mixed** | The locale (i.e. fr-FR). |





***

### processDefinition

Processes the number format definition for the provided locale.

```php
protected processDefinition(string $locale, array $definition): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale. |
| `$definition` | **array** | The definition |


**Return Value:**

The processed definition.




***

### getDefinitions

Gets the number format definitions.

```php
protected getDefinitions(): array
```









**Return Value:**


The number format definitions, keyed by locale.




***


***
> Automatically generated on 2025-03-15
