
# SimplePie_Credit

Handles `<media:credit>` as defined in Media RSS



* Full name: `\SimplePie_Credit`
* Parent class: [`\SimplePie\Credit`](./SimplePie/Credit.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct

Constructor, used to input the data

```php
public __construct(mixed $role = null, mixed $scheme = null, mixed $name = null): mixed
```

For documentation on all the parameters, see the corresponding
properties and their accessors






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$role` | **mixed** |  |
| `$scheme` | **mixed** |  |
| `$name` | **mixed** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_role

Get the role of the person receiving credit

```php
public get_role(): string|null
```












***

### get_scheme

Get the organizational scheme

```php
public get_scheme(): string|null
```












***

### get_name

Get the credited person/entity's name

```php
public get_name(): string|null
```












***


***
> Automatically generated on 2025-03-18
