
# HTMLPurifier_ChildDef_List

Definition for list containers ul and ol.

What does this do?  The big thing is to handle ol/ul at the top
level of list nodes, which should be handled specially by /folding/
them into the previous list node.  We generally shouldn't ever
see other disallowed elements, because the autoclose behavior
in MakeWellFormed handles it.

* Full name: `\HTMLPurifier_ChildDef_List`
* Parent class: [`\HTMLPurifier_ChildDef`](./HTMLPurifier_ChildDef.md)



## Properties


### type

Type of child definition, usually right-most part of class name lowercase.

```php
public $type
```






***

### elements

Lookup array of all elements that this definition could possibly allow.

```php
public $elements
```






***

### whitespace



```php
public $whitespace
```






***

## Methods


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
> Automatically generated on 2025-03-15
