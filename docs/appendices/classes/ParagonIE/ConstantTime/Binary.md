
# Binary

Class Binary

Binary string operators that don't choke on
mbstring.func_overload

* Full name: `\ParagonIE\ConstantTime\Binary`
* This class is an **Abstract class**




## Methods


### safeStrlen

Safe string length

```php
public static safeStrlen(string $str): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***

### safeSubstr

Safe substring

```php
public static safeSubstr(string $str, int $start, ?int $length = null): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |
| `$start` | **int** |  |
| `$length` | **?int** |  |




**Throws:**

- [`TypeError`](../../TypeError.md)



***


***
> Automatically generated on 2025-03-18
