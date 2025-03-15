***

# UUIDUtil

UUID Utility.

This class has static methods to generate and validate UUID's.
UUIDs are used a decent amount within various *DAV standards, so it made
sense to include it.

* Full name: `\Sabre\DAV\UUIDUtil`




## Methods


### getUUID

Returns a pseudo-random v4 UUID.

```php
public static getUUID(): string
```

This function is based on a comment by Andrew Moore on php.net

* This method is **static**.








**See Also:**

* http://www.php.net/manual/en/function.uniqid.php#94959 - 

***

### validateUUID

Checks if a string is a valid UUID.

```php
public static validateUUID(string $uuid): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **string** |  |





***


***
> Automatically generated on 2025-03-15
