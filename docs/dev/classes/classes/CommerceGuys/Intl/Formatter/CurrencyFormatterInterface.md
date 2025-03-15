***

# CurrencyFormatterInterface





* Full name: `\CommerceGuys\Intl\Formatter\CurrencyFormatterInterface`



## Methods


### format

Formats a currency amount.

```php
public format(string $number, string $currencyCode, array $options = []): string
```

Supported options:
- locale:                  The locale. Default: 'en'.
- use_grouping:            Whether to use grouping separators,
                           such as thousands separators.
                           Default: true.
- minimum_fraction_digits: Minimum fraction digits.
- maximum_fraction_digits: Minimum fraction digits.
- rounding_mode:           The rounding mode.
                           A PHP_ROUND_ constant or 'none' to skip
                           rounding. Default: PHP_ROUND_HALF_UP.
- style:                   The style.
                           One of: 'standard', 'accounting'.
                           Default: 'standard'.
- currency_display:        How the currency should be displayed.
                           One of: 'code', 'symbol', 'none'.
                           Default: 'symbol'.

Both minimum_fraction_digits and maximum_fraction_digits default
to the currency's number of fraction digits.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |
| `$currencyCode` | **string** | The currency code. |
| `$options` | **array** | The formatting options. |


**Return Value:**

The formatted number.




***

### parse

Parses a formatted currency amount.

```php
public parse(string $number, string $currencyCode, array $options = []): string|false
```

Commonly used in input widgets where the end-user might input
a number using digits and symbols common to their locale.

Supported options:
- locale: The locale. Default: 'en'.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The formatted number. |
| `$currencyCode` | **string** | The currency code. |
| `$options` | **array** | The parsing options. |


**Return Value:**

The parsed number or FALSE on error.




***


***
> Automatically generated on 2025-03-15
