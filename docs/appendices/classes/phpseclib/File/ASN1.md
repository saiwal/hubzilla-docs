
# ASN1

Pure-PHP ASN.1 Parser



* Full name: `\phpseclib\File\ASN1`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`CLASS_UNIVERSAL`|public| |0|
|`CLASS_APPLICATION`|public| |1|
|`CLASS_CONTEXT_SPECIFIC`|public| |2|
|`CLASS_PRIVATE`|public| |3|
|`TYPE_BOOLEAN`|public| |1|
|`TYPE_INTEGER`|public| |2|
|`TYPE_BIT_STRING`|public| |3|
|`TYPE_OCTET_STRING`|public| |4|
|`TYPE_NULL`|public| |5|
|`TYPE_OBJECT_IDENTIFIER`|public| |6|
|`TYPE_REAL`|public| |9|
|`TYPE_ENUMERATED`|public| |10|
|`TYPE_UTF8_STRING`|public| |12|
|`TYPE_SEQUENCE`|public| |16|
|`TYPE_SET`|public| |17|
|`TYPE_NUMERIC_STRING`|public| |18|
|`TYPE_PRINTABLE_STRING`|public| |19|
|`TYPE_TELETEX_STRING`|public| |20|
|`TYPE_VIDEOTEX_STRING`|public| |21|
|`TYPE_IA5_STRING`|public| |22|
|`TYPE_UTC_TIME`|public| |23|
|`TYPE_GENERALIZED_TIME`|public| |24|
|`TYPE_GRAPHIC_STRING`|public| |25|
|`TYPE_VISIBLE_STRING`|public| |26|
|`TYPE_GENERAL_STRING`|public| |27|
|`TYPE_UNIVERSAL_STRING`|public| |28|
|`TYPE_BMP_STRING`|public| |30|
|`TYPE_CHOICE`|public| |-1|
|`TYPE_ANY`|public| |-2|

## Properties


### oids

ASN.1 object identifier

```php
public array $oids
```





**See Also:**

* http://en.wikipedia.org/wiki/Object_identifier - 

***

### format

Default date format

```php
public string $format
```





**See Also:**

* http://php.net/class.datetime - 

***

### encoded

Default date format

```php
public array $encoded
```





**See Also:**

* \phpseclib\File\self::setTimeFormat() - * \phpseclib\File\self::asn1map() - * http://php.net/class.datetime - 

***

### filters

Filters

```php
public array $filters
```

If the mapping type is self::TYPE_ANY what do we actually encode it as?



**See Also:**

* \phpseclib\File\self::_encode_der() - 

***

### location

Current Location of most recent ASN.1 encode process

```php
public array $location
```

Useful for debug purposes



**See Also:**

* \phpseclib\File\self::encode_der() - 

***

### ANYmap

Type mapping table for the ANY type.

```php
public array $ANYmap
```

Structured or unknown types are mapped to a \phpseclib\File\ASN1\Element.
Unambiguous types get the direct mapping (int/real/bool).
Others are mapped as a choice, with an extra indexing level.




***

### stringTypeSize

String type to character size mapping table.

```php
public array $stringTypeSize
```

Non-convertable types are absent from this table.
size == 0 indicates variable length encoding.




***

## Methods


### decodeBER

Parse BER-encoding

```php
public decodeBER(string $encoded): array
```

Serves a similar purpose to openssl's asn1parse






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoded` | **string** |  |





***

### _decode_ber

Parse BER-encoding (Helper function)

```php
public _decode_ber(string $encoded, int $start, int $encoded_pos): array
```

Sometimes we want to get the BER encoding of a particular tag.  $start lets us do that without having to reencode.
$encoded is passed by reference for the recursive calls done for self::TYPE_BIT_STRING and
self::TYPE_OCTET_STRING. In those cases, the indefinite length is used.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoded` | **string** |  |
| `$start` | **int** |  |
| `$encoded_pos` | **int** |  |





***

### asn1map

ASN.1 Map

```php
public asn1map(array $decoded, array $mapping, array $special = array()): array
```

Provides an ASN.1 semantic mapping ($mapping) from a parsed BER-encoding to a human readable format.

"Special" mappings may be applied on a per tag-name basis via $special.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$decoded` | **array** |  |
| `$mapping` | **array** |  |
| `$special` | **array** |  |





***

### encodeDER

ASN.1 Encode

```php
public encodeDER(string $source, string $mapping, array $special = array()): string
```

DER-encodes an ASN.1 semantic mapping ($mapping).  Some libraries would probably call this function
an ASN.1 compiler.

"Special" mappings can be applied via $special.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |
| `$mapping` | **string** |  |
| `$special` | **array** |  |





***

### _encode_der

ASN.1 Encode (Helper function)

```php
public _encode_der(string $source, string $mapping, int $idx = null, array $special = array()): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |
| `$mapping` | **string** |  |
| `$idx` | **int** |  |
| `$special` | **array** |  |





***

### _encodeLength

DER-encode the length

```php
public _encodeLength(int $length): string
```

DER supports lengths up to (2**8)**127, however, we'll only support lengths up to (2**8)**4.  See
{@link http://itu.int/ITU-T/studygroups/com17/languages/X.690-0207.pdf#p=13} for more information.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** |  |





***

### _decodeOID

BER-decode the OID

```php
public _decodeOID(string $content): string
```

Called by _decode_ber()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **string** |  |





***

### _encodeOID

DER-encode the OID

```php
public _encodeOID(string $source): string
```

Called by _encode_der()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |





***

### _decodeTime

BER-decode the time

```php
public _decodeTime(string $content, int $tag): string
```

Called by _decode_ber() and in the case of implicit tags asn1map().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **string** |  |
| `$tag` | **int** |  |





***

### setTimeFormat

Set the time format

```php
public setTimeFormat(string $format): mixed
```

Sets the time / date format for asn1map().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **string** |  |





***

### loadOIDs

Load OIDs

```php
public loadOIDs(array $oids): mixed
```

Load the relevant OIDs for a particular ASN.1 semantic mapping.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oids` | **array** |  |





***

### loadFilters

Load filters

```php
public loadFilters(array $filters): mixed
```

See \phpseclib\File\X509, etc, for an example.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filters` | **array** |  |





***

### _string_shift

String Shift

```php
public _string_shift(string& $string, int $index = 1): string
```

Inspired by array_shift






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$index` | **int** |  |





***

### convert

String type conversion

```php
public convert(string $in, int $from = self::TYPE_UTF8_STRING, int $to = self::TYPE_UTF8_STRING): string
```

This is a lazy conversion, dealing only with character size.
No real conversion table is used.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **string** |  |
| `$from` | **int** |  |
| `$to` | **int** |  |





***


***
> Automatically generated on 2025-03-18
