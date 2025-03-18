***

# VersionTrait

Provides common functionality for handling the version, as defined by RFC 4122



* Full name: `\Ramsey\Uuid\Rfc4122\VersionTrait`




## Methods


### getVersion

Returns the version

```php
public getVersion(): ?int
```




* This method is **abstract**.







***

### isMax

Returns true if these fields represent a max UUID

```php
public isMax(): bool
```




* This method is **abstract**.







***

### isNil

Returns true if these fields represent a nil UUID

```php
public isNil(): bool
```




* This method is **abstract**.







***

### isCorrectVersion

Returns true if the version matches one of those defined by RFC 4122

```php
private isCorrectVersion(): bool
```









**Return Value:**

True if the UUID version is valid, false otherwise




***

***
> Automatically generated on 2025-03-18

