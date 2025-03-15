
# Credit

Handles `<media:credit>` as defined in Media RSS

Used by {@see \SimplePie\Enclosure::get_credit()} and {@see \SimplePie\Enclosure::get_credits()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_credit_class()}

* Full name: `\SimplePie\Credit`



## Properties


### role

Credited role

```php
public string $role
```





**See Also:**

* \SimplePie\get_role() - 

***

### scheme

Organizational scheme

```php
public string $scheme
```





**See Also:**

* \SimplePie\get_scheme() - 

***

### name

Credited name

```php
public string $name
```





**See Also:**

* \SimplePie\get_name() - 

***

## Methods


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
> Automatically generated on 2025-03-15
