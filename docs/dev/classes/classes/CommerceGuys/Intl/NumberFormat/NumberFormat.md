
# NumberFormat

Provides metadata for number formatting.



* Full name: `\CommerceGuys\Intl\NumberFormat\NumberFormat`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`NUMBERING_SYSTEM_ARABIC`|public| |&#039;arab&#039;|
|`NUMBERING_SYSTEM_ARABIC_EXTENDED`|public| |&#039;arabext&#039;|
|`NUMBERING_SYSTEM_BENGALI`|public| |&#039;beng&#039;|
|`NUMBERING_SYSTEM_DEVANAGARI`|public| |&#039;deva&#039;|
|`NUMBERING_SYSTEM_LATIN`|public| |&#039;latn&#039;|

## Properties


### locale

The locale (i.e. "en_US").

```php
protected string $locale
```






***

### decimalPattern

The number pattern used to format decimal numbers.

```php
protected string $decimalPattern
```






***

### percentPattern

The number pattern used to format percentages.

```php
protected string $percentPattern
```






***

### currencyPattern

The number pattern used to format currency amounts.

```php
protected string $currencyPattern
```






***

### accountingCurrencyPattern

The number pattern used to format accounting currency amounts.

```php
protected string $accountingCurrencyPattern
```






***

### numberingSystem

The numbering system.

```php
protected string $numberingSystem
```






***

### decimalSeparator

The decimal separator.

```php
protected string $decimalSeparator
```






***

### decimalCurrencySeparator

The decimal separator for currency amounts.

```php
protected string $decimalCurrencySeparator
```






***

### groupingSeparator

The grouping separator.

```php
protected string $groupingSeparator
```






***

### groupingCurrencySeparator

The grouping separator for currency amounts.

```php
protected string $groupingCurrencySeparator
```






***

### plusSign

The plus sign.

```php
protected string $plusSign
```






***

### minusSign

The number symbols.

```php
protected string $minusSign
```






***

### percentSign

The percent sign.

```php
protected string $percentSign
```






***

## Methods


### __construct

Creates a new NumberFormat instance.

```php
public __construct(array $definition): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$definition` | **array** | The definition array. |





***

### getLocale

Gets the locale.

```php
public getLocale(): string
```












***

### getDecimalPattern

Gets the number pattern used to format decimal numbers.

```php
public getDecimalPattern(): string
```












**See Also:**

* http://cldr.unicode.org/translation/number-patterns - 

***

### getPercentPattern

Gets the number pattern used to format percentages.

```php
public getPercentPattern(): string
```












**See Also:**

* http://cldr.unicode.org/translation/number-patterns - 

***

### getCurrencyPattern

Gets the number pattern used to format currency amounts.

```php
public getCurrencyPattern(): string
```












**See Also:**

* http://cldr.unicode.org/translation/number-patterns - 

***

### getAccountingCurrencyPattern

Gets the number pattern used to format accounting currency amounts.

```php
public getAccountingCurrencyPattern(): string
```

Most commonly used when formatting amounts on invoices.










**See Also:**

* http://cldr.unicode.org/translation/number-patterns - 

***

### getNumberingSystem

Gets the numbering system.

```php
public getNumberingSystem(): string
```

The value is one of the NUMBERING_SYSTEM_ constants.










***

### getDecimalSeparator

Gets the decimal separator.

```php
public getDecimalSeparator(): string
```












***

### getDecimalCurrencySeparator

Gets the decimal separator for currency amounts.

```php
public getDecimalCurrencySeparator(): string
```












***

### getGroupingSeparator

Gets the grouping separator for currency amounts.

```php
public getGroupingSeparator(): string
```












***

### getGroupingCurrencySeparator

Gets the currency grouping separator.

```php
public getGroupingCurrencySeparator(): string
```












***

### getPlusSign

Gets the plus sign.

```php
public getPlusSign(): string
```












***

### getMinusSign

Gets the minus sign.

```php
public getMinusSign(): string
```












***

### getPercentSign

Gets the percent sign.

```php
public getPercentSign(): string
```












***


***
> Automatically generated on 2025-03-15
