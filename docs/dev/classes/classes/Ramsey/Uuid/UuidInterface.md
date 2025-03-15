
# UuidInterface

A UUID is a universally unique identifier adhering to an agreed-upon
representation format and standard for generation



* Full name: `\Ramsey\Uuid\UuidInterface`
* Parent interfaces: [`\Ramsey\Uuid\DeprecatedUuidInterface`](./DeprecatedUuidInterface.md), [`JsonSerializable`](../../JsonSerializable.md), [`Serializable`](../../Serializable.md), [`Stringable`](../../Stringable.md)


## Methods


### compareTo

Returns -1, 0, or 1 if the UUID is less than, equal to, or greater than
the other UUID

```php
public compareTo(\Ramsey\Uuid\UuidInterface $other): int&lt;-1, 1&gt;
```

The first of two UUIDs is greater than the second if the most
significant field in which the UUIDs differ is greater for the first
UUID.

* Q. What's the value of being able to sort UUIDs?
* A. Use them as keys in a B-Tree or similar mapping.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **\Ramsey\Uuid\UuidInterface** | The UUID to compare |


**Return Value:**

-1, 0, or 1 if the UUID is less than, equal to, or greater than $other




***

### equals

Returns true if the UUID is equal to the provided object

```php
public equals(object|null $other): bool
```

The result is true if and only if the argument is not null, is a UUID
object, has the same variant, and contains the same value, bit for bit,
as the UUID.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$other` | **object&#124;null** | An object to test for equality with this UUID |


**Return Value:**

True if the other object is equal to this UUID




***

### getBytes

Returns the binary string representation of the UUID

```php
public getBytes(): string
```












***

### getFields

Returns the fields that comprise this UUID

```php
public getFields(): \Ramsey\Uuid\Fields\FieldsInterface
```












***

### getHex

Returns the hexadecimal representation of the UUID

```php
public getHex(): \Ramsey\Uuid\Type\Hexadecimal
```












***

### getInteger

Returns the integer representation of the UUID

```php
public getInteger(): \Ramsey\Uuid\Type\Integer
```












***

### getUrn

Returns the string standard representation of the UUID as a URN

```php
public getUrn(): string
```












**See Also:**

* http://en.wikipedia.org/wiki/Uniform_Resource_Name - Uniform Resource Name* https://tools.ietf.org/html/rfc4122#section-3 - RFC 4122, § 3: Namespace Registration Template

***

### toString

Returns the string standard representation of the UUID

```php
public toString(): string
```












***

### __toString

Casts the UUID to the string standard representation

```php
public __toString(): string
```












***


## Inherited methods


### getNumberConverter



```php
public getNumberConverter(): \Ramsey\Uuid\Converter\NumberConverterInterface
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getFieldsHex



```php
public getFieldsHex(): string[]
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSeqHiAndReservedHex



```php
public getClockSeqHiAndReservedHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSeqLowHex



```php
public getClockSeqLowHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getClockSequenceHex



```php
public getClockSequenceHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getDateTime



```php
public getDateTime(): \DateTimeInterface
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getLeastSignificantBitsHex



```php
public getLeastSignificantBitsHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getMostSignificantBitsHex



```php
public getMostSignificantBitsHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getNodeHex



```php
public getNodeHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeHiAndVersionHex



```php
public getTimeHiAndVersionHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeLowHex



```php
public getTimeLowHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimeMidHex



```php
public getTimeMidHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getTimestampHex



```php
public getTimestampHex(): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getVariant



```php
public getVariant(): ?int
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### getVersion



```php
public getVersion(): ?int
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***


***
> Automatically generated on 2025-03-15
