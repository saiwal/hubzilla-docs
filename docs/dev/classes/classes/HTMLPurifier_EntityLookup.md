***

# HTMLPurifier_EntityLookup

Object that provides entity lookup table from entity name to character



* Full name: `\HTMLPurifier_EntityLookup`



## Properties


### table

Assoc array of entity name to character represented.

```php
public $table
```






***

## Methods


### setup

Sets up the entity lookup table from the serialized file contents.

```php
public setup(bool $file = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **bool** |  |





***

### instance

Retrieves sole instance of the object.

```php
public static instance(bool|\HTMLPurifier_EntityLookup $prototype = false): \HTMLPurifier_EntityLookup
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **bool&#124;\HTMLPurifier_EntityLookup** | Optional prototype of custom lookup table to overload with. |





***


***
> Automatically generated on 2025-03-15
