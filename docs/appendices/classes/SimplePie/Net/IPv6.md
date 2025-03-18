
# IPv6

Class to validate and to work with IPv6 addresses.



* Full name: `\SimplePie\Net\IPv6`

**See Also:**

* http://pear.php.net/package/Net_IPv6 - 




## Methods


### uncompress

Uncompresses an IPv6 address

```php
public static uncompress(string $ip): string
```

RFC 4291 allows you to compress concecutive zero pieces in an address to
'::'. This method expects a valid IPv6 address and expands the '::' to
the required number of zero pieces.

Example:  FF01::101   ->  FF01:0:0:0:0:0:0:101
          ::1         ->  0:0:0:0:0:0:0:1

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ip` | **string** | An IPv6 address |


**Return Value:**

The uncompressed IPv6 address




***

### compress

Compresses an IPv6 address

```php
public static compress(string $ip): string
```

RFC 4291 allows you to compress concecutive zero pieces in an address to
'::'. This method expects a valid IPv6 address and compresses consecutive
zero pieces to '::'.

Example:  FF01:0:0:0:0:0:0:101   ->  FF01::101
          0:0:0:0:0:0:0:1        ->  ::1

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ip` | **string** | An IPv6 address |


**Return Value:**

The compressed IPv6 address




**See Also:**

* \SimplePie\Net\uncompress() - 

***

### split_v6_v4

Splits an IPv6 address into the IPv6 and IPv4 representation parts

```php
private static split_v6_v4(string $ip): array
```

RFC 4291 allows you to represent the last two parts of an IPv6 address
using the standard IPv4 representation

Example:  0:0:0:0:0:0:13.1.68.3
          0:0:0:0:0:FFFF:129.144.52.38

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ip` | **string** | An IPv6 address |


**Return Value:**

[0] contains the IPv6 represented part, and [1] the IPv4 represented part




***

### check_ipv6

Checks an IPv6 address

```php
public static check_ipv6(string $ip): bool
```

Checks if the given IP is a valid IPv6 address

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ip` | **string** | An IPv6 address |


**Return Value:**

true if $ip is a valid IPv6 address




***

### checkIPv6

Checks if the given IP is a valid IPv6 address

```php
public static checkIPv6(string $ip): bool
```



* This method is **static**.


* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ip` | **string** | An IPv6 address |


**Return Value:**

true if $ip is a valid IPv6 address




**See Also:**

* \SimplePie\Net\check_ipv6 - 

***


***
> Automatically generated on 2025-03-18
