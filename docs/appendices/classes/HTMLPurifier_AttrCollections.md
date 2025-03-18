
# HTMLPurifier_AttrCollections

Defines common attribute collections that modules reference



* Full name: `\HTMLPurifier_AttrCollections`



## Properties


### info

Associative array of attribute collections, indexed by name.

```php
public $info
```






***

## Methods


### __construct

Performs all expansions on internal data for use by other inclusions
It also collects all attribute collection extensions from
modules

```php
public __construct(\HTMLPurifier_AttrTypes $attr_types, \HTMLPurifier_HTMLModule[] $modules): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr_types` | **\HTMLPurifier_AttrTypes** | HTMLPurifier_AttrTypes instance |
| `$modules` | **\HTMLPurifier_HTMLModule[]** | Hash array of HTMLPurifier_HTMLModule members |





***

### doConstruct



```php
public doConstruct(mixed $attr_types, mixed $modules): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr_types` | **mixed** |  |
| `$modules` | **mixed** |  |





***

### performInclusions

Takes a reference to an attribute associative array and performs
all inclusions specified by the zero index.

```php
public performInclusions(array& $attr): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** | Reference to attribute array |





***

### expandIdentifiers

Expands all string identifiers in an attribute array by replacing
them with the appropriate values inside HTMLPurifier_AttrTypes

```php
public expandIdentifiers(array& $attr, \HTMLPurifier_AttrTypes $attr_types): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** | Reference to attribute array |
| `$attr_types` | **\HTMLPurifier_AttrTypes** | HTMLPurifier_AttrTypes instance |





***


***
> Automatically generated on 2025-03-18
