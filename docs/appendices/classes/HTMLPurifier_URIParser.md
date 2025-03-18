
# HTMLPurifier_URIParser

Parses a URI into the components and fragment identifier as specified
by RFC 3986.



* Full name: `\HTMLPurifier_URIParser`



## Properties


### percentEncoder

Instance of HTMLPurifier_PercentEncoder to do normalization with.

```php
protected $percentEncoder
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### parse

Parses a URI.

```php
public parse(mixed $uri): \HTMLPurifier_URI
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **mixed** | string URI to parse |


**Return Value:**

representation of URI. This representation has
not been validated yet and may not conform to RFC.




***


***
> Automatically generated on 2025-03-18
