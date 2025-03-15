***

# HTMLPurifier_PropertyList

Generic property list implementation



* Full name: `\HTMLPurifier_PropertyList`



## Properties


### data

Internal data-structure for properties.

```php
protected $data
```






***

### parent

Parent plist.

```php
protected $parent
```






***

### cache

Cache.

```php
protected $cache
```






***

## Methods


### __construct



```php
public __construct(\HTMLPurifier_PropertyList $parent = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parent` | **\HTMLPurifier_PropertyList** | Parent plist |





***

### get

Recursively retrieves the value for a key

```php
public get(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### set

Sets the value of a key, for this plist

```php
public set(string $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### has

Returns true if a given key exists

```php
public has(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### reset

Resets a value to the value of it's parent, usually the default. If
no value is specified, the entire plist is reset.

```php
public reset(string $name = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### squash

Squashes this property list and all of its property lists into a single
array, and returns the array. This value is cached by default.

```php
public squash(bool $force = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$force` | **bool** | If true, ignores the cache and regenerates the array. |





***

### getParent

Returns the parent plist.

```php
public getParent(): \HTMLPurifier_PropertyList
```












***

### setParent

Sets the parent plist.

```php
public setParent(\HTMLPurifier_PropertyList $plist): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plist` | **\HTMLPurifier_PropertyList** | Parent plist |





***


***
> Automatically generated on 2025-03-15
