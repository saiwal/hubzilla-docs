
# Currency

Represents a currency.



* Full name: `\CommerceGuys\Intl\Currency\Currency`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### currencyCode

The alphanumeric currency code.

```php
protected string $currencyCode
```






***

### name

The currency name.

```php
protected string $name
```






***

### numericCode

The numeric currency code.

```php
protected string $numericCode
```






***

### symbol

The currency symbol.

```php
protected string $symbol
```






***

### fractionDigits

The number of fraction digits.

```php
protected int $fractionDigits
```






***

### locale

The locale (i.e. "en_US").

```php
protected string $locale
```






***

## Methods


### __construct

Creates a new Currency instance.

```php
public __construct(array $definition): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$definition` | **array** | The definition array. |





***

### __toString

Gets the string representation of the currency.

```php
public __toString(): string
```












***

### getCurrencyCode

Gets the alphabetic currency code.

```php
public getCurrencyCode(): string
```












***

### getName

Gets the currency name.

```php
public getName(): string
```

This value is locale specific.










***

### getNumericCode

Gets the numeric currency code.

```php
public getNumericCode(): string
```

The numeric code has three digits, and the first one can be a zero,
hence the need to pass it around as a string.










***

### getSymbol

Gets the currency symbol.

```php
public getSymbol(): string
```

This value is locale specific.










***

### getFractionDigits

Gets the number of fraction digits.

```php
public getFractionDigits(): int
```

Used when rounding or formatting an amount for display.
Actual storage precision can be greater.










***

### getLocale

Gets the locale.

```php
public getLocale(): string
```

The currency name and symbol are locale specific.










***


***
> Automatically generated on 2025-03-15
