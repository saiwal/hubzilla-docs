***

# Restriction

Handles `<media:restriction>` as defined in Media RSS

Used by {@see \SimplePie\Enclosure::get_restriction()} and {@see \SimplePie\Enclosure::get_restrictions()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_restriction_class()}

* Full name: `\SimplePie\Restriction`



## Properties


### relationship

Relationship ('allow'/'deny')

```php
public string $relationship
```





**See Also:**

* \SimplePie\get_relationship() - 

***

### type

Type of restriction

```php
public string $type
```





**See Also:**

* \SimplePie\get_type() - 

***

### value

Restricted values

```php
public string $value
```





**See Also:**

* \SimplePie\get_value() - 

***

## Methods


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
> Automatically generated on 2025-03-15
