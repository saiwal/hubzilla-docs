
# HTMLPurifier_IDAccumulator

Component of HTMLPurifier_AttrContext that accumulates IDs to prevent dupes



* Full name: `\HTMLPurifier_IDAccumulator`



## Properties


### ids

Lookup table of IDs we've accumulated.

```php
public $ids
```






***

## Methods


### build

Builds an IDAccumulator, also initializing the default blacklist

```php
public static build(\HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_IDAccumulator
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** | Instance of HTMLPurifier_Config |
| `$context` | **\HTMLPurifier_Context** | Instance of HTMLPurifier_Context |


**Return Value:**

Fully initialized HTMLPurifier_IDAccumulator




***

### add

Add an ID to the lookup table.

```php
public add(string $id): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | ID to be added. |


**Return Value:**

status, true if success, false if there's a dupe




***

### load

Load a list of IDs into the lookup table

```php
public load(mixed $array_of_ids): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array_of_ids` | **mixed** | Array of IDs to load |





***


***
> Automatically generated on 2025-03-18
