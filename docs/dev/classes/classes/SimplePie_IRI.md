
# SimplePie_IRI

IRI parser/serialiser/normaliser



* Full name: `\SimplePie_IRI`
* Parent class: [`\SimplePie\IRI`](./SimplePie/IRI.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __toString

Return the entire IRI when you try and read the object as a string

```php
public __toString(): string
```












***

### __set

Overload __set() to provide access via properties

```php
public __set(string $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Property name |
| `$value` | **mixed** | Property value |





***

### __get

Overload __get() to provide access via properties

```php
public __get(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Property name |





***

### __isset

Overload __isset() to provide access via properties

```php
public __isset(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Property name |





***

### __unset

Overload __unset() to provide access via properties

```php
public __unset(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Property name |





***

### __construct

Create a new IRI object, from a specified string

```php
public __construct(string $iri = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iri` | **string** |  |





***

### __destruct

Clean up

```php
public __destruct(): mixed
```












***

### absolutize

Create a new IRI object by resolving a relative IRI

```php
public static absolutize(\SimplePie\IRI|string $base, \SimplePie\IRI|string $relative): \SimplePie\IRI|false
```

Returns false if $base is not absolute, otherwise an IRI.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base` | **\SimplePie\IRI&#124;string** | (Absolute) Base IRI |
| `$relative` | **\SimplePie\IRI&#124;string** | Relative IRI |





***

### parse_iri

Parse an IRI into scheme/authority/path/query/fragment segments

```php
protected parse_iri(string $iri): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iri` | **string** |  |





***

### remove_dot_segments

Remove dot segments from a path

```php
protected remove_dot_segments(string $input): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** |  |





***

### replace_invalid_with_pct_encoding

Replace invalid character with percent encoding

```php
protected replace_invalid_with_pct_encoding(string $string, string $extra_chars, bool $iprivate = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | Input string |
| `$extra_chars` | **string** | Valid characters not in iunreserved or<br />iprivate (this is ASCII-only) |
| `$iprivate` | **bool** | Allow iprivate |





***

### remove_iunreserved_percent_encoded

Callback function for preg_replace_callback.

```php
protected remove_iunreserved_percent_encoded(array $match): string
```

Removes sequences of percent encoded bytes that represent UTF-8
encoded characters in iunreserved






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$match` | **array** | PCRE match |


**Return Value:**

Replacement




***

### scheme_normalization



```php
protected scheme_normalization(): mixed
```












***

### is_valid

Check if the object represents a valid IRI. This needs to be done on each
call as some things change depending on another part of the IRI.

```php
public is_valid(): bool
```












***

### set_iri

Set the entire IRI. Returns true on success, false on failure (if there
are any invalid characters).

```php
public set_iri(string $iri, mixed $clear_cache = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iri` | **string** |  |
| `$clear_cache` | **mixed** |  |





***

### set_scheme

Set the scheme. Returns true on success, false on failure (if there are
any invalid characters).

```php
public set_scheme(string $scheme): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scheme` | **string** |  |





***

### set_authority

Set the authority. Returns true on success, false on failure (if there are
any invalid characters).

```php
public set_authority(string $authority, mixed $clear_cache = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$authority` | **string** |  |
| `$clear_cache` | **mixed** |  |





***

### set_userinfo

Set the iuserinfo.

```php
public set_userinfo(string $iuserinfo): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iuserinfo` | **string** |  |





***

### set_host

Set the ihost. Returns true on success, false on failure (if there are
any invalid characters).

```php
public set_host(string $ihost): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ihost` | **string** |  |





***

### set_port

Set the port. Returns true on success, false on failure (if there are
any invalid characters).

```php
public set_port(string $port): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$port` | **string** |  |





***

### set_path

Set the ipath.

```php
public set_path(string $ipath, mixed $clear_cache = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ipath` | **string** |  |
| `$clear_cache` | **mixed** |  |





***

### set_query

Set the iquery.

```php
public set_query(string $iquery): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iquery` | **string** |  |





***

### set_fragment

Set the ifragment.

```php
public set_fragment(string $ifragment): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ifragment` | **string** |  |





***

### to_uri

Convert an IRI to a URI (or parts thereof)

```php
public to_uri(mixed $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |





***

### get_iri

Get the complete IRI

```php
public get_iri(): string
```












***

### get_uri

Get the complete URI

```php
public get_uri(): string
```












***

### get_iauthority

Get the complete iauthority

```php
protected get_iauthority(): string
```












***

### get_authority

Get the complete authority

```php
protected get_authority(): string
```












***


***
> Automatically generated on 2025-03-15
