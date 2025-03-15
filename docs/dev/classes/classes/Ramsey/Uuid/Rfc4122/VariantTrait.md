***

# VariantTrait

Provides common functionality for handling the variant, as defined by RFC 4122



* Full name: `\Ramsey\Uuid\Rfc4122\VariantTrait`




## Methods


### getBytes

Returns the bytes that comprise the fields

```php
public getBytes(): string
```




* This method is **abstract**.







***

### getVariant

Returns the variant identifier, according to RFC 4122, for the given bytes

```php
public getVariant(): int
```

The following values may be returned:

- `0` -- Reserved, NCS backward compatibility.
- `2` -- The variant specified in RFC 4122.
- `6` -- Reserved, Microsoft Corporation backward compatibility.
- `7` -- Reserved for future definition.







**Return Value:**

The variant identifier, according to RFC 4122




**See Also:**

* https://tools.ietf.org/html/rfc4122#section-4.1.1 - RFC 4122, § 4.1.1: Variant

***

***
> Automatically generated on 2025-03-15

