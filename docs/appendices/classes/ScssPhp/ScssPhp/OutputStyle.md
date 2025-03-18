
# OutputStyle





* Full name: `\ScssPhp\ScssPhp\OutputStyle`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`EXPANDED`|public| |&#039;expanded&#039;|
|`COMPRESSED`|public| |&#039;compressed&#039;|


## Methods


### fromString

Converts a string to an output style.

```php
public static fromString(string $string): self::*
```

Using this method allows to write code which will support both
versions 1.12+ and 2.0 of Scssphp. In 2.0, OutputStyle will be
an enum instead of using string constants.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |





***

### toString

Converts an output style to a string supported by {@see OutputStyle::fromString()}.

```php
public static toString(self::* $outputStyle): string
```

Using this method allows to write code which will support both
versions 1.12+ and 2.0 of Scssphp. In 2.0, OutputStyle will be
an enum instead of using string constants.
The returned string representation is guaranteed to be compatible
between 1.12 and 2.0.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$outputStyle` | **self::*** |  |





***


***
> Automatically generated on 2025-03-18
