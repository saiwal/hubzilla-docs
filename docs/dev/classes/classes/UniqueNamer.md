***

# UniqueNamer

A UniqueNamer issues unique names, keeping track of any previously issued
names.



* Full name: `\UniqueNamer`



## Properties


### prefix

Constructs a new UniqueNamer.

```php
public $prefix
```






***

### counter



```php
public $counter
```






***

### existing



```php
public $existing
```






***

### order



```php
public $order
```






***

## Methods


### __construct



```php
public __construct(mixed $prefix): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefix` | **mixed** |  |





***

### __clone

Clones this UniqueNamer.

```php
public __clone(): mixed
```












***

### getName

Gets the new name for the given old name, where if no old name is given
a new name will be generated.

```php
public getName(mixed $old_name = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$old_name` | **mixed** |  |


**Return Value:**

the new name.




***

### isNamed

Returns true if the given old name has already been assigned a new name.

```php
public isNamed(string $old_name): true
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$old_name` | **string** | the old name to check. |


**Return Value:**

if the old name has been assigned a new name, false if not.




***


***
> Automatically generated on 2025-03-15
