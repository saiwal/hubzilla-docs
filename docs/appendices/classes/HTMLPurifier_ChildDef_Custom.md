
# HTMLPurifier_ChildDef_Custom

Custom validation class, accepts DTD child definitions



* Full name: `\HTMLPurifier_ChildDef_Custom`
* Parent class: [`\HTMLPurifier_ChildDef`](./HTMLPurifier_ChildDef.md)



## Properties


### type

Type of child definition, usually right-most part of class name lowercase.

```php
public $type
```






***

### allow_empty

Indicates whether or not an empty array of children is okay.

```php
public $allow_empty
```






***

### dtd_regex

Allowed child pattern as defined by the DTD.

```php
public $dtd_regex
```






***

### _pcre_regex

PCRE regex derived from $dtd_regex.

```php
private $_pcre_regex
```






***

## Methods


### __construct



```php
public __construct(mixed $dtd_regex): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dtd_regex` | **mixed** | Allowed child pattern from the DTD |





***

### _compileRegex

Compiles the PCRE regex from a DTD regex ($dtd_regex to $_pcre_regex)

```php
protected _compileRegex(): mixed
```












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
> Automatically generated on 2025-03-18
