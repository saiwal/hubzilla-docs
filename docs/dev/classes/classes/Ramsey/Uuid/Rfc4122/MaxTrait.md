***

# MaxTrait

Provides common functionality for max UUIDs

The max UUID is special form of UUID that is specified to have all 128 bits
set to one. It is the inverse of the nil UUID.

* Full name: `\Ramsey\Uuid\Rfc4122\MaxTrait`

**See Also:**

* https://datatracker.ietf.org/doc/html/draft-ietf-uuidrev-rfc4122bis-00#section-5.10 - Max UUID




## Methods


### getBytes

Returns the bytes that comprise the fields

```php
public getBytes(): string
```




* This method is **abstract**.







***

### isMax

Returns true if the byte string represents a max UUID

```php
public isMax(): bool
```












***

***
> Automatically generated on 2025-03-15

