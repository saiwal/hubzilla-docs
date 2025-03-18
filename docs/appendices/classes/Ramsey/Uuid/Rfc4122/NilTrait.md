***

# NilTrait

Provides common functionality for nil UUIDs

The nil UUID is special form of UUID that is specified to have all 128 bits
set to zero.

* Full name: `\Ramsey\Uuid\Rfc4122\NilTrait`

**See Also:**

* https://tools.ietf.org/html/rfc4122#section-4.1.7 - RFC 4122, § 4.1.7: Nil UUID




## Methods


### getBytes

Returns the bytes that comprise the fields

```php
public getBytes(): string
```




* This method is **abstract**.







***

### isNil

Returns true if the byte string represents a nil UUID

```php
public isNil(): bool
```












***

***
> Automatically generated on 2025-03-18

