***

# CallableNameFilter

Creating a cache filename with callables



* Full name: `\SimplePie\Cache\CallableNameFilter`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\SimplePie\Cache\NameFilter`](./NameFilter.md)
* This class is a **Final class**



## Properties


### callable



```php
private callable $callable
```






***

## Methods


### __construct



```php
public __construct(callable $callable): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$callable` | **callable** |  |





***

### filter

Method to create cache filename with.

```php
public filter(string $name): string
```

The returning name MUST follow the rules for keys in PSR-16.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | The name for the cache will be most likly an url with query string |


**Return Value:**

the new cache name




**See Also:**

* https://www.php-fig.org/psr/psr-16/ - The returning name MUST be a string of at least one character
that uniquely identifies a cached item, MUST only contain the
characters A-Z, a-z, 0-9, _, and . in any order in UTF-8 encoding
and MUST not longer then 64 characters. The following characters
are reserved for future extensions and MUST NOT be used: }()/\@:

A provided implementing library MAY support additional characters
and encodings or longer lengths, but MUST support at least that
minimum.

***


***
> Automatically generated on 2025-03-15
