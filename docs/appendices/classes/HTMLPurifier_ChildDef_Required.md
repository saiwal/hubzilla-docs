
# HTMLPurifier_ChildDef_Required

Definition that allows a set of elements, but disallows empty children.



* Full name: `\HTMLPurifier_ChildDef_Required`
* Parent class: [`\HTMLPurifier_ChildDef`](./HTMLPurifier_ChildDef.md)



## Properties


### elements

Lookup table of allowed elements.

```php
public $elements
```






***

### whitespace

Whether or not the last passed node was all whitespace.

```php
protected $whitespace
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

## Methods


### __construct



```php
public __construct(array|string $elements): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$elements` | **array&#124;string** | List of allowed element names (lowercase). |





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
public validateChildren(\HTMLPurifier_Node[] $children, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool|array
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$children` | **\HTMLPurifier_Node[]** | Array of HTMLPurifier_Node |
| `$config` | **\HTMLPurifier_Config** | HTMLPurifier_Config object |
| `$context` | **\HTMLPurifier_Context** | HTMLPurifier_Context object |


**Return Value:**

true to leave nodes as is, false to remove parent node, array of replacement children




***


***
> Automatically generated on 2025-03-18
