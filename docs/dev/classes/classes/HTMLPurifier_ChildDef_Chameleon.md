***

# HTMLPurifier_ChildDef_Chameleon

Definition that uses different definitions depending on context.

The del and ins tags are notable because they allow different types of
elements depending on whether or not they're in a block or inline context.
Chameleon allows this behavior to happen by using two different
definitions depending on context.  While this somewhat generalized,
it is specifically intended for those two tags.

* Full name: `\HTMLPurifier_ChildDef_Chameleon`
* Parent class: [`\HTMLPurifier_ChildDef`](./HTMLPurifier_ChildDef.md)



## Properties


### inline

Instance of the definition object to use when inline. Usually stricter.

```php
public $inline
```






***

### block

Instance of the definition object to use when block.

```php
public $block
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
public __construct(array $inline, array $block): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inline` | **array** | List of elements to allow when inline. |
| `$block` | **array** | List of elements to allow when block. |





***

### validateChildren

Validates nodes according to definition and returns modification.

```php
public validateChildren(\HTMLPurifier_Node[] $children, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$children` | **\HTMLPurifier_Node[]** |  |
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
> Automatically generated on 2025-03-15
