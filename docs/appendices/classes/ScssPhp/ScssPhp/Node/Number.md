
# Number

Dimension + optional units

}

* Full name: `\ScssPhp\ScssPhp\Node\Number`
* Parent class: [`Node`](../Node.md)
* This class implements:
[`\ArrayAccess`](../../../ArrayAccess.md), [`\JsonSerializable`](../../../JsonSerializable.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`PRECISION`|public| |10|

## Properties


### precision



```php
public static int $precision
```



* This property is **static**.
* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### unitTable



```php
protected static array $unitTable
```



* This property is **static**.

**See Also:**

* http://www.w3.org/TR/2012/WD-css3-values-20120308/ - 

***

### dimension



```php
private int|float $dimension
```






***

### numeratorUnits



```php
private string[] $numeratorUnits
```






***

### denominatorUnits



```php
private string[] $denominatorUnits
```






***

## Methods


### __construct

Initialize number

```php
public __construct(int|float $dimension, string[]|string $numeratorUnits, string[] $denominatorUnits = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dimension` | **int&#124;float** |  |
| `$numeratorUnits` | **string[]&#124;string** |  |
| `$denominatorUnits` | **string[]** |  |





***

### getDimension



```php
public getDimension(): float|int
```












***

### getNumeratorUnits



```php
public getNumeratorUnits(): list&lt;string&gt;
```












***

### getDenominatorUnits



```php
public getDenominatorUnits(): list&lt;string&gt;
```












***

### jsonSerialize



```php
public jsonSerialize(): mixed
```












***

### offsetExists



```php
public offsetExists(mixed $offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |





***

### offsetGet



```php
public offsetGet(mixed $offset): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |





***

### offsetSet



```php
public offsetSet(mixed $offset, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |
| `$value` | **mixed** |  |





***

### offsetUnset



```php
public offsetUnset(mixed $offset): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **mixed** |  |





***

### unitless

Returns true if the number is unitless

```php
public unitless(): bool
```












***

### hasUnits

Returns true if the number has any units

```php
public hasUnits(): bool
```












***

### hasUnit

Checks whether the number has exactly this unit

```php
public hasUnit(string $unit): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$unit` | **string** |  |





***

### unitStr

Returns unit(s) as the product of numerator units divided by the product of denominator units

```php
public unitStr(): string
```












***

### valueInRange



```php
public valueInRange(float|int $min, float|int $max, string|null $name = null): float|int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$min` | **float&#124;int** |  |
| `$max` | **float&#124;int** |  |
| `$name` | **string&#124;null** |  |




**Throws:**

- [`SassScriptException`](../Exception/SassScriptException.md)



***

### assertNoUnits



```php
public assertNoUnits(string|null $varName = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$varName` | **string&#124;null** |  |





***

### assertUnit



```php
public assertUnit(string $unit, string|null $varName = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$unit` | **string** |  |
| `$varName` | **string&#124;null** |  |





***

### assertSameUnitOrUnitless



```php
public assertSameUnitOrUnitless(\ScssPhp\ScssPhp\Node\Number $other): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### coerce

Returns a copy of this number, converted to the units represented by $newNumeratorUnits and $newDenominatorUnits.

```php
public coerce(string[] $newNumeratorUnits, string[] $newDenominatorUnits): \ScssPhp\ScssPhp\Node\Number
```

This does not throw an error if this number is unitless and
$newNumeratorUnits/$newDenominatorUnits are not empty, or vice versa. Instead,
it treats all unitless numbers as convertible to and from all units without
changing the value.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$newNumeratorUnits` | **string[]** |  |
| `$newDenominatorUnits` | **string[]** |  |




**Throws:**
<p>if this number's units are not compatible with $newNumeratorUnits and $newDenominatorUnits</p>

- [`SassScriptException`](../Exception/SassScriptException.md)



***

### isComparableTo



```php
public isComparableTo(\ScssPhp\ScssPhp\Node\Number $other): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### lessThan



```php
public lessThan(\ScssPhp\ScssPhp\Node\Number $other): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### lessThanOrEqual



```php
public lessThanOrEqual(\ScssPhp\ScssPhp\Node\Number $other): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### greaterThan



```php
public greaterThan(\ScssPhp\ScssPhp\Node\Number $other): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### greaterThanOrEqual



```php
public greaterThanOrEqual(\ScssPhp\ScssPhp\Node\Number $other): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### plus



```php
public plus(\ScssPhp\ScssPhp\Node\Number $other): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### minus



```php
public minus(\ScssPhp\ScssPhp\Node\Number $other): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### unaryMinus



```php
public unaryMinus(): \ScssPhp\ScssPhp\Node\Number
```












***

### modulo



```php
public modulo(\ScssPhp\ScssPhp\Node\Number $other): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### times



```php
public times(\ScssPhp\ScssPhp\Node\Number $other): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### dividedBy



```php
public dividedBy(\ScssPhp\ScssPhp\Node\Number $other): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### equals



```php
public equals(\ScssPhp\ScssPhp\Node\Number $other): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### output

Output number

```php
public output(\ScssPhp\ScssPhp\Compiler $compiler = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compiler` | **\ScssPhp\ScssPhp\Compiler** |  |





***

### __toString

{@inheritdoc}

```php
public __toString(): mixed
```












***

### coerceNumber



```php
private coerceNumber(\ScssPhp\ScssPhp\Node\Number $other, callable $operation): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$operation` | **callable** |  |





***

### coerceUnits



```php
private coerceUnits(\ScssPhp\ScssPhp\Node\Number $other, callable $operation): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$operation` | **callable** |  |





***

### valueInUnits



```php
private valueInUnits(string[] $numeratorUnits, string[] $denominatorUnits): int|float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numeratorUnits` | **string[]** |  |
| `$denominatorUnits` | **string[]** |  |




**Throws:**
<p>if this number's units are not compatible with $numeratorUnits and $denominatorUnits</p>

- [`SassScriptException`](../Exception/SassScriptException.md)



***

### multiplyUnits



```php
private multiplyUnits(int|float $value, string[] $numerators1, string[] $denominators1, string[] $numerators2, string[] $denominators2): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **int&#124;float** |  |
| `$numerators1` | **string[]** |  |
| `$denominators1` | **string[]** |  |
| `$numerators2` | **string[]** |  |
| `$denominators2` | **string[]** |  |





***

### getConversionFactor

Returns the number of [unit1]s per [unit2].

```php
private static getConversionFactor(string $unit1, string $unit2): float|int|null
```

Equivalently, `1unit1 * conversionFactor(unit1, unit2) = 1unit2`.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$unit1` | **string** |  |
| `$unit2` | **string** |  |





***

### getUnitString

Returns unit(s) as the product of numerator units divided by the product of denominator units

```php
private static getUnitString(string[] $numerators, string[] $denominators): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numerators` | **string[]** |  |
| `$denominators` | **string[]** |  |





***


***
> Automatically generated on 2025-03-18
