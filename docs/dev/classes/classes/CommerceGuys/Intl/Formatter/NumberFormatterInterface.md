***

# NumberFormatterInterface





* Full name: `\CommerceGuys\Intl\Formatter\NumberFormatterInterface`



## Methods


### format

Formats a number.

```php
public format(string $number, array $options = []): string
```

Supported options:
- locale:                  The locale. Default: 'en'.
- use_grouping:            Whether to use grouping separators,
                           such as thousands separators.
                           Default: true.
- minimum_fraction_digits: Minimum fraction digits. Default: 0.
- maximum_fraction_digits: Minimum fraction digits. Default: 3.
- rounding_mode:           The rounding mode.
                           A PHP_ROUND_ constant or 'none' to skip
                           rounding. Default: PHP_ROUND_HALF_UP.
- style:                   The style.
                           One of: 'decimal', 'percent'.
                           Default: 'decimal'.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The number. |
| `$options` | **array** | The formatting options. |


**Return Value:**

The formatted number.




***

### parse

Parses a number.

```php
public parse(string $number, array $options = []): string|false
```

Commonly used in input widgets where the end-user might input
a number using digits and symbols common to their locale.

Supported options:
- locale: The locale. Default: 'en'.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number` | **string** | The formatted number. |
| `$options` | **array** | The parsing options. |


**Return Value:**

The parsed number or FALSE on error.




***


***
> Automatically generated on 2025-03-15
