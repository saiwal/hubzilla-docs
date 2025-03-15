
# RoundingMode

Specifies a rounding behavior for numerical operations capable of discarding precision.

Each rounding mode indicates how the least significant returned digit of a rounded result
is to be calculated. If fewer digits are returned than the digits needed to represent the
exact numerical result, the discarded digits will be referred to as the discarded fraction
regardless the digits' contribution to the value of the number. In other words, considered
as a numerical value, the discarded fraction could have an absolute value greater than one.

* Full name: `\Brick\Math\RoundingMode`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`UNNECESSARY`|public| |0|
|`UP`|public| |1|
|`DOWN`|public| |2|
|`CEILING`|public| |3|
|`FLOOR`|public| |4|
|`HALF_UP`|public| |5|
|`HALF_DOWN`|public| |6|
|`HALF_CEILING`|public| |7|
|`HALF_FLOOR`|public| |8|
|`HALF_EVEN`|public| |9|


## Methods


### __construct

Private constructor. This class is not instantiable.

```php
private __construct(): mixed
```












***


***
> Automatically generated on 2025-03-15
