
# StringUtil

Useful utilities for working with various strings.



* Full name: `\Sabre\VObject\StringUtil`




## Methods


### isUTF8

Returns true or false depending on if a string is valid UTF-8.

```php
public static isUTF8(string $str): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***

### convertToUTF8

This method tries its best to convert the input string to UTF-8.

```php
public static convertToUTF8(string $str): string
```

Currently only ISO-5991-1 input and UTF-8 input is supported, but this
may be expanded upon if we receive other examples.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***


***
> Automatically generated on 2025-03-18
