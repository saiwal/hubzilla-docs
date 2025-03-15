
# HTMLPurifier_ChildDef

Defines allowed child nodes and validates nodes against it.



* Full name: `\HTMLPurifier_ChildDef`
* This class is an **Abstract class**



## Properties


### type

Type of child definition, usually right-most part of class name lowercase.

```php
public $type
```

Used occasionally in terms of context.




***

### allow_empty

Indicates whether or not an empty array of children is okay.

```php
public $allow_empty
```

This is necessary for redundant checking when changes affecting
a child node may cause a parent node to now be disallowed.




***

### elements

Lookup array of all elements that this definition could possibly allow.

```php
public $elements
```






***

## Methods


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
