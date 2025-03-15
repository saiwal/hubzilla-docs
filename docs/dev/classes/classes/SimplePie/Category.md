***

# Category

Manages all category-related data

Used by {@see \SimplePie\Item::get_category()} and {@see \SimplePie\Item::get_categories()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_category_class()}

* Full name: `\SimplePie\Category`



## Properties


### term

Category identifier

```php
public string|null $term
```





**See Also:**

* \SimplePie\get_term - 

***

### scheme

Categorization scheme identifier

```php
public string|null $scheme
```





**See Also:**

* \SimplePie\get_scheme() - 

***

### label

Human readable label

```php
public string|null $label
```





**See Also:**

* \SimplePie\get_label() - 

***

### type

Category type

```php
public string|null $type
```

category for <category>
subject for <dc:subject>



**See Also:**

* \SimplePie\get_type() - 

***

## Methods


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
