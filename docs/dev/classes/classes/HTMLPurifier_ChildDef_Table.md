***

# HTMLPurifier_ChildDef_Table

Definition for tables.  The general idea is to extract out all of the
essential bits, and then reconstruct it later.

This is a bit confusing, because the DTDs and the W3C
validators seem to disagree on the appropriate definition. The
DTD claims:

     (CAPTION?, (COL*|COLGROUP*), THEAD?, TFOOT?, TBODY+)

But actually, the HTML4 spec then has this to say:

     The TBODY start tag is always required except when the table
     contains only one table body and no table head or foot sections.
     The TBODY end tag may always be safely omitted.

So the DTD is kind of wrong.  The validator is, unfortunately, kind
of on crack.

The definition changed again in XHTML1.1; and in my opinion, this
formulation makes the most sense.

     caption?, ( col* | colgroup* ), (( thead?, tfoot?, tbody+ ) | ( tr+ ))

Essentially, we have two modes: thead/tfoot/tbody mode, and tr mode.
If we encounter a thead, tfoot or tbody, we are placed in the former
mode, and we *must* wrap any stray tr segments with a tbody. But if
we don't run into any of them, just have tr tags is OK.

* Full name: `\HTMLPurifier_ChildDef_Table`
* Parent class: [`\HTMLPurifier_ChildDef`](./HTMLPurifier_ChildDef.md)



## Properties


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

### elements

Lookup array of all elements that this definition could possibly allow.

```php
public $elements
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












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
> Automatically generated on 2025-03-15
