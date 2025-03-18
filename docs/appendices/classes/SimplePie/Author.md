
# Author

Manages all author-related data

Used by {@see \SimplePie\Item::get_author()} and {@see \SimplePie\SimplePie::get_authors()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_author_class()}

* Full name: `\SimplePie\Author`



## Properties


### name

Author's name

```php
public string $name
```





**See Also:**

* \SimplePie\get_name() - 

***

### link

Author's link

```php
public string $link
```





**See Also:**

* \SimplePie\get_link() - 

***

### email

Author's email address

```php
public string $email
```





**See Also:**

* \SimplePie\get_email() - 

***

## Methods


### __construct

Constructor, used to input the data

```php
public __construct(string $name = null, string $link = null, string $email = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$link` | **string** |  |
| `$email` | **string** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_name

Author's name

```php
public get_name(): string|null
```












***

### get_link

Author's link

```php
public get_link(): string|null
```












***

### get_email

Author's email address

```php
public get_email(): string|null
```












***


***
> Automatically generated on 2025-03-18
