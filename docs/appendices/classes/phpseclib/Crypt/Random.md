
# Random

Pure-PHP Random Number Generator



* Full name: `\phpseclib\Crypt\Random`




## Methods


### string

Generate a random string.

```php
public static string(int $length): string
```

Although microoptimizations are generally discouraged as they impair readability this function is ripe with
microoptimizations because this function has the potential of being called a huge number of times.
eg. for RSA key generation.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** |  |





***


***
> Automatically generated on 2025-03-18
