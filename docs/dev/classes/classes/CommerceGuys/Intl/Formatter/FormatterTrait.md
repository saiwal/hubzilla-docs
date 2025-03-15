***

# FormatterTrait





* Full name: `\CommerceGuys\Intl\Formatter\FormatterTrait`



## Properties


### parsedPatterns

The parsed number patterns, keyed by locale and style.

```php
protected \CommerceGuys\Intl\Formatter\ParsedPattern[] $parsedPatterns
```






***

### digits

Localized digits.

```php
protected array $digits
```






***

## Methods


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

