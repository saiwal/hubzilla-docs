***

# ValueConverter





* Full name: `\ScssPhp\ScssPhp\ValueConverter`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**




## Methods


### __construct



```php
private __construct(): mixed
```












***

### parseValue

Parses a value from a Scss source string.

```php
public static parseValue(string $source): mixed
```

The returned value is guaranteed to be supported by the
Compiler methods for registering custom variables. No other
guarantee about it is provided. It should be considered
opaque values by the caller.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |





***

### fromPhp

Converts a PHP value to a Sass value

```php
public static fromPhp(mixed $value): mixed
```

The returned value is guaranteed to be supported by the
Compiler methods for registering custom variables. No other
guarantee about it is provided. It should be considered
opaque values by the caller.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
