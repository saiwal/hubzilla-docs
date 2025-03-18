
# SimplePie_Restriction

Handles `<media:restriction>` as defined in Media RSS



* Full name: `\SimplePie_Restriction`
* Parent class: [`\SimplePie\Restriction`](./SimplePie/Restriction.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct

Constructor, used to input the data

```php
public __construct(mixed $relationship = null, mixed $type = null, mixed $value = null): mixed
```

For documentation on all the parameters, see the corresponding
properties and their accessors






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$relationship` | **mixed** |  |
| `$type` | **mixed** |  |
| `$value` | **mixed** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_relationship

Get the relationship

```php
public get_relationship(): string|null
```









**Return Value:**

Either 'allow' or 'deny'




***

### get_type

Get the type

```php
public get_type(): string|null
```












***

### get_value

Get the list of restricted things

```php
public get_value(): string|null
```












***


***
> Automatically generated on 2025-03-18
