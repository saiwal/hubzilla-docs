
# SimplePie_Rating

Handles `<media:rating>` or `<itunes:explicit>` tags as defined in Media RSS and iTunes RSS respectively



* Full name: `\SimplePie_Rating`
* Parent class: [`\SimplePie\Rating`](./SimplePie/Rating.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


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
