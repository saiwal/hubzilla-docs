
# NameFilter

Interface for creating a cache filename



* Full name: `\SimplePie\Cache\NameFilter`



## Methods


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
> Automatically generated on 2025-03-18
