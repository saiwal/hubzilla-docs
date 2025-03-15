***

# ASN_BASE





* Full name: `\ASN_BASE`



## Properties


### asnData



```php
public $asnData
```






***

### cursor



```php
private $cursor
```






***

### parent



```php
private $parent
```






***

### ASN_MARKERS



```php
public static $ASN_MARKERS
```



* This property is **static**.


***

### ASN_TYPES



```php
public static $ASN_TYPES
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(mixed $v = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** |  |





***

### setParent



```php
public setParent(mixed $parent): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parent` | **mixed** |  |





***

### generateSubclasses

This function will take the markers and types arrays and
dynamically generate classes that extend this class for each one,
and also define constants for them.

```php
public static generateSubclasses(): mixed
```



* This method is **static**.








***

### makeSubclass

Helper function for generateSubclasses()

```php
public static makeSubclass(mixed $name, mixed $bit): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$bit` | **mixed** |  |





***

### reset

This function reset's the internal cursor used for value iteration.

```php
public reset(): mixed
```












***

### __get

This function catches calls to get the value for the type, typeName, value, values, and data
from the object.  For type calls we just return the class name or the value of the constant that
is named the same as the class.

```php
public __get(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### parseASNString

Parse an ASN.1 binary string.

```php
public static parseASNString(string $string = false, int $level = 1, mixed $maxLevels = false): \ASN_BASE
```

This function takes a binary ASN.1 string and parses it into it's respective
pieces and returns it.  It can optionally stop at any depth.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | The binary ASN.1 String |
| `$level` | **int** | The current parsing depth level |
| `$maxLevels` | **mixed** |  |


**Return Value:**

The array representation of the ASN.1 data contained in $string




***

### parseASNData

Parse an ASN.1 field value.

```php
public static parseASNData(int $type, string $data, int $level, int $maxLevels): mixed
```

This function takes a binary ASN.1 value and parses it according to it's specified type

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** | The type of data being provided |
| `$data` | **string** | The raw binary data string |
| `$level` | **int** | The current parsing depth |
| `$maxLevels` | **int** | The max parsing depth |


**Return Value:**

The data that was parsed from the raw binary data string




***

### parseOID

Parse an ASN.1 OID value.

```php
public static parseOID(mixed $string): string
```

This takes the raw binary string that represents an OID value and parses it into its
dot notation form.  example - 1.2.840.113549.1.1.5
look up OID's here: http://www.oid-info.com/
(the multi-byte OID section can be done in a more efficient way, I will fix it later)

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |


**Return Value:**

The OID contained in $data




***

### printASN



```php
public static printASN(mixed $x, mixed $indent = &#039;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |
| `$indent` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
