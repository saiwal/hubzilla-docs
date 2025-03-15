
# Copyright

Manages `<media:copyright>` copyright tags as defined in Media RSS

Used by {@see \SimplePie\Enclosure::get_copyright()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_copyright_class()}

* Full name: `\SimplePie\Copyright`



## Properties


### url

Copyright URL

```php
public string $url
```





**See Also:**

* \SimplePie\get_url() - 

***

### label

Attribution

```php
public string $label
```





**See Also:**

* \SimplePie\get_attribution() - 

***

## Methods


### __construct

Constructor, used to input the data

```php
public __construct(mixed $url = null, mixed $label = null): mixed
```

For documentation on all the parameters, see the corresponding
properties and their accessors






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$label` | **mixed** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_url

Get the copyright URL

```php
public get_url(): string|null
```









**Return Value:**

URL to copyright information




***

### get_attribution

Get the attribution text

```php
public get_attribution(): string|null
```












***


***
> Automatically generated on 2025-03-15
