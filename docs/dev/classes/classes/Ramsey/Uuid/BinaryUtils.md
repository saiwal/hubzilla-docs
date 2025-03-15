***

# BinaryUtils

Provides binary math utilities



* Full name: `\Ramsey\Uuid\BinaryUtils`




## Methods


### applyVariant

Applies the RFC 4122 variant field to the 16-bit clock sequence

```php
public static applyVariant(int $clockSeq): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clockSeq` | **int** | The 16-bit clock sequence value before the RFC 4122<br />variant is applied |


**Return Value:**

The 16-bit clock sequence multiplexed with the UUID variant




**See Also:**

* http://tools.ietf.org/html/rfc4122#section-4.1.1 - RFC 4122, § 4.1.1: Variant

***

### applyVersion

Applies the RFC 4122 version number to the 16-bit `time_hi_and_version` field

```php
public static applyVersion(int $timeHi, int $version): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timeHi` | **int** | The value of the 16-bit `time_hi_and_version` field<br />before the RFC 4122 version is applied |
| `$version` | **int** | The RFC 4122 version to apply to the `time_hi` field |


**Return Value:**

The 16-bit time_hi field of the timestamp multiplexed with
the UUID version number




**See Also:**

* http://tools.ietf.org/html/rfc4122#section-4.1.3 - RFC 4122, § 4.1.3: Version

***


***
> Automatically generated on 2025-03-15
