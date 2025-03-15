***

# HTMLPurifier_AttrTypes

Provides lookup array of attribute types to HTMLPurifier_AttrDef objects



* Full name: `\HTMLPurifier_AttrTypes`



## Properties


### info

Lookup array of attribute string identifiers to concrete implementations.

```php
protected $info
```






***

## Methods


### __construct

Constructs the info array, supplying default implementations for attribute
types.

```php
public __construct(): mixed
```












***

### makeEnum



```php
private static makeEnum(mixed $in): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$in` | **mixed** |  |





***

### get

Retrieves a type

```php
public get(string $type): \HTMLPurifier_AttrDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | String type name |


**Return Value:**

Object AttrDef for type




***

### set

Sets a new implementation for a type

```php
public set(string $type, \HTMLPurifier_AttrDef $impl): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | String type name |
| `$impl` | **\HTMLPurifier_AttrDef** | Object AttrDef for type |





***


***
> Automatically generated on 2025-03-15
