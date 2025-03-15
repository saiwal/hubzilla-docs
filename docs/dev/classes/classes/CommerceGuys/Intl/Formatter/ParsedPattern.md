
# ParsedPattern

Represents a parsed number pattern.



* Full name: `\CommerceGuys\Intl\Formatter\ParsedPattern`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### positivePattern

The positive number pattern.

```php
protected string $positivePattern
```






***

### negativePattern

The negative number pattern.

```php
protected string $negativePattern
```






***

### groupingUsed

Whether grouping is used.

```php
protected bool $groupingUsed
```






***

### primaryGroupSize

The primary group size.

```php
protected int $primaryGroupSize
```






***

### secondaryGroupSize

The secondary group size.

```php
protected int $secondaryGroupSize
```






***

## Methods


### __construct

Creates a new ParsedPattern instance.

```php
public __construct(string $pattern): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pattern` | **string** | The raw pattern. |





***

### getPositivePattern

Gets the positive number pattern.

```php
public getPositivePattern(): string
```

Used to format positive numbers.










***

### getNegativePattern

Gets the negative number pattern.

```php
public getNegativePattern(): string
```

Used to format negative numbers.










***

### isGroupingUsed

Gets whether grouping is used.

```php
public isGroupingUsed(): bool
```

Indicates that major digits should be grouped according to
group sizes, right-to-left.










***

### getPrimaryGroupSize

Gets the primary group size.

```php
public getPrimaryGroupSize(): int|null
```












***

### getSecondaryGroupSize

Gets the secondary group size.

```php
public getSecondaryGroupSize(): int|null
```












***


***
> Automatically generated on 2025-03-15
