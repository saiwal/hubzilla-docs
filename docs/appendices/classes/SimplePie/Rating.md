
# Rating

Handles `<media:rating>` or `<itunes:explicit>` tags as defined in Media RSS and iTunes RSS respectively

Used by {@see \SimplePie\Enclosure::get_rating()} and {@see \SimplePie\Enclosure::get_ratings()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_rating_class()}

* Full name: `\SimplePie\Rating`



## Properties


### scheme

Rating scheme

```php
public string $scheme
```





**See Also:**

* \SimplePie\get_scheme() - 

***

### value

Rating value

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
public __construct(mixed $scheme = null, mixed $value = null): mixed
```

For documentation on all the parameters, see the corresponding
properties and their accessors






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scheme` | **mixed** |  |
| `$value` | **mixed** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_scheme

Get the organizational scheme for the rating

```php
public get_scheme(): string|null
```












***

### get_value

Get the value of the rating

```php
public get_value(): string|null
```












***


***
> Automatically generated on 2025-03-18
