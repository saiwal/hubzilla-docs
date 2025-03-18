
# HTMLPurifier_ChildDef_StrictBlockquote

Takes the contents of blockquote when in strict and reformats for validation.



* Full name: `\HTMLPurifier_ChildDef_StrictBlockquote`
* Parent class: [`\HTMLPurifier_ChildDef_Required`](./HTMLPurifier_ChildDef_Required.md)



## Properties


### real_elements



```php
protected $real_elements
```






***

### fake_elements



```php
protected $fake_elements
```






***

### allow_empty

Indicates whether or not an empty array of children is okay.

```php
public $allow_empty
```






***

### type

Type of child definition, usually right-most part of class name lowercase.

```php
public $type
```






***

### init



```php
protected $init
```






***

## Methods


### getAllowedElements

Get lookup of tag names that should not close this element automatically.

```php
public getAllowedElements(\HTMLPurifier_Config $config): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### validateChildren

Validates nodes according to definition and returns modification.

```php
public validateChildren(array $children, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$children` | **array** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### init



```php
private init(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


## Inherited methods


### getAllowedElements

Get lookup of tag names that should not close this element automatically.

```php
public getAllowedElements(\HTMLPurifier_Config $config): array
```

All other elements will do so.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** | HTMLPurifier_Config object |





***

### validateChildren

Validates nodes according to definition and returns modification.

```php
public validateChildren(array $children, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$children` | **array** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### __construct



```php
public __construct(array|string $elements): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$elements` | **array&#124;string** | List of allowed element names (lowercase). |





***


***
> Automatically generated on 2025-03-18
