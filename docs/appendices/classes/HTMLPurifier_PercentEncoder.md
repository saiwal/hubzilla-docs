
# HTMLPurifier_PercentEncoder

Class that handles operations involving percent-encoding in URIs.



* Full name: `\HTMLPurifier_PercentEncoder`



## Properties


### preserve

Reserved characters to preserve when using encode().

```php
protected $preserve
```






***

## Methods


### __construct

String of characters that should be preserved while using encode().

```php
public __construct(bool $preserve = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$preserve` | **bool** |  |





***

### encode

Our replacement for urlencode, it encodes all non-reserved characters,
as well as any extra characters that were instructed to be preserved.

```php
public encode(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to be encoded |


**Return Value:**

Encoded string.




***

### normalize

Fix up percent-encoding by decoding unreserved characters and normalizing.

```php
public normalize(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to normalize |





***


***
> Automatically generated on 2025-03-18
