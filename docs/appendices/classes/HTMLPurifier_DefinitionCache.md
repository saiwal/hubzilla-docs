
# HTMLPurifier_DefinitionCache

Abstract class representing Definition cache managers that implements
useful common methods and is a factory.



* Full name: `\HTMLPurifier_DefinitionCache`
* This class is an **Abstract class**



## Properties


### type



```php
public $type
```






***

## Methods


### __construct



```php
public __construct(string $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | Type of definition objects this instance of the<br />cache will handle. |





***

### generateKey

Generates a unique identifier for a particular configuration

```php
public generateKey(\HTMLPurifier_Config $config): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** | Instance of HTMLPurifier_Config |





***

### isOld

Tests whether or not a key is old with respect to the configuration's
version and revision number.

```php
public isOld(string $key, \HTMLPurifier_Config $config): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | Key to test |
| `$config` | **\HTMLPurifier_Config** | Instance of HTMLPurifier_Config to test against |





***

### checkDefType

Checks if a definition's type jives with the cache's type

```php
public checkDefType(\HTMLPurifier_Definition $def): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** | Definition object to check |


**Return Value:**

true if good, false if not




***

### add

Adds a definition object to the cache

```php
public add(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### set

Unconditionally saves a definition object to the cache

```php
public set(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### replace

Replace an object in the cache

```php
public replace(\HTMLPurifier_Definition $def, \HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_Definition** |  |
| `$config` | **\HTMLPurifier_Config** |  |





***

### get

Retrieves a definition object from the cache

```php
public get(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### remove

Removes a definition object to the cache

```php
public remove(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### flush

Clears all objects from cache

```php
public flush(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### cleanup

Clears all expired (older version or revision) objects from cache

```php
public cleanup(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


***
> Automatically generated on 2025-03-18
