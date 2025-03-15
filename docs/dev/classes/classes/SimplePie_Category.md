
# SimplePie_Category

Manages all category-related data



* Full name: `\SimplePie_Category`
* Parent class: [`\SimplePie\Category`](./SimplePie/Category.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct

Constructor, used to input the data

```php
public __construct(string|null $term = null, string|null $scheme = null, string|null $label = null, string|null $type = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$term` | **string&#124;null** |  |
| `$scheme` | **string&#124;null** |  |
| `$label` | **string&#124;null** |  |
| `$type` | **string&#124;null** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_term

Get the category identifier

```php
public get_term(): string|null
```












***

### get_scheme

Get the categorization scheme identifier

```php
public get_scheme(): string|null
```












***

### get_label

Get the human readable label

```php
public get_label(bool $strict = false): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$strict` | **bool** |  |





***

### get_type

Get the category type

```php
public get_type(): string|null
```












***


***
> Automatically generated on 2025-03-15
