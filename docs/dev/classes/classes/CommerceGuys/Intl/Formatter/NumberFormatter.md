
# NumberFormatter

Formats numbers using locale-specific patterns.



* Full name: `\CommerceGuys\Intl\Formatter\NumberFormatter`
* This class implements:
[`\CommerceGuys\Intl\Formatter\NumberFormatterInterface`](./NumberFormatterInterface.md)



## Properties


### numberFormatRepository

The number format repository.

```php
protected \CommerceGuys\Intl\NumberFormat\NumberFormatRepositoryInterface $numberFormatRepository
```






***

### defaultOptions

The default options.

```php
protected array $defaultOptions
```






***

### numberFormats

The loaded number formats.

```php
protected \CommerceGuys\Intl\NumberFormat\NumberFormat[] $numberFormats
```






***

## Methods


### __construct

Creates a NumberFormatter instance.

```php
public __construct(\CommerceGuys\Intl\NumberFormat\NumberFormatRepositoryInterface $numberFormatRepository, array $defaultOptions = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberFormatRepository` | **\CommerceGuys\Intl\NumberFormat\NumberFormatRepositoryInterface** | The number format repository. |
| `$defaultOptions` | **array** | The default options. |




**Throws:**

- [`InvalidArgumentException`](../../../InvalidArgumentException.md)

- [`RuntimeException`](../../../RuntimeException.md)



***

### format

Formats a number.

```php
public format(mixed $number, array $options = []): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **mixed** | The number. |
| `$options` | **array** | The formatting options. |


**Return Value:**

The formatted number.




***

### parse

Parses a number.

```php
public parse(mixed $number, array $options = []): string|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **mixed** | The formatted number. |
| `$options` | **array** | The parsing options. |


**Return Value:**

The parsed number or FALSE on error.




***

### getNumberFormat

Gets the number format for the provided locale.

```php
protected getNumberFormat(string $locale): \CommerceGuys\Intl\NumberFormat\NumberFormat
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locale` | **string** | The locale. |





***

### getAvailablePatterns

{@inheritdoc}

```php
protected getAvailablePatterns(\CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** |  |





***

### validateOptions

Validates the provided options.

```php
protected validateOptions(array $options): mixed
```

Ensures the absence of unknown keys, correct data types and values.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **array** | The options. |




**Throws:**

- [`InvalidArgumentException`](../../../InvalidArgumentException.md)



***

### getLocalizedSymbols

{@inheritdoc}

```php
protected getLocalizedSymbols(\CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** |  |





***


## Inherited methods


### formatNumber

Formats the number according to the number format.

```php
protected formatNumber(string $number, \CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat, array $options = []): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** | The number format. |
| `$options` | **array** |  |


**Return Value:**

The formatted number.




***

### localizeNumber

Localizes the number according to the number format.

```php
protected localizeNumber(string $number, \CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat): string
```

Both the digits and the symbols are replaced
with their localized equivalents.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** | The number format. |


**Return Value:**

The localized number.




**See Also:**

* http://cldr.unicode.org/translation/number-symbols - 

***

### parseNumber

Parses the number according to the number format.

```php
protected parseNumber(string $number, \CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat): string
```

Both the digits and the symbols are replaced
with their non-localized equivalents.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** | The number format. |


**Return Value:**

The localized number.




***

### getParsedPattern

Gets the pattern for the provided number format.

```php
protected getParsedPattern(\CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat, string $style): \CommerceGuys\Intl\Formatter\ParsedPattern
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** | The number format. |
| `$style` | **string** | The formatter style. |





***

### getAvailablePatterns

Gets the available patterns for the provided number format.

```php
protected getAvailablePatterns(\CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat): string[]
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** | The number format. |


**Return Value:**

The patterns, keyed by style.




***

### getLocalizedSymbols

Gets the localized symbols for the provided number format.

```php
protected getLocalizedSymbols(\CommerceGuys\Intl\NumberFormat\NumberFormat $numberFormat): array
```

Used to localize the number in localizeNumber().


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberFormat` | **\CommerceGuys\Intl\NumberFormat\NumberFormat** | The number format. |





***


***
> Automatically generated on 2025-03-15
