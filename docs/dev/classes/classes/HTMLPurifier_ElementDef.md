
# HTMLPurifier_ElementDef

Structure that stores an HTML element definition. Used by
HTMLPurifier_HTMLDefinition and HTMLPurifier_HTMLModule.



* Full name: `\HTMLPurifier_ElementDef`



## Properties


### standalone

Does the definition work by itself, or is it created solely
for the purpose of merging into another definition?

```php
public $standalone
```






***

### attr

Associative array of attribute name to HTMLPurifier_AttrDef.

```php
public $attr
```






***

### attr_transform_pre

List of tags HTMLPurifier_AttrTransform to be done before validation.

```php
public $attr_transform_pre
```






***

### attr_transform_post

List of tags HTMLPurifier_AttrTransform to be done after validation.

```php
public $attr_transform_post
```






***

### child

HTMLPurifier_ChildDef of this tag.

```php
public $child
```






***

### content_model

Abstract string representation of internal ChildDef rules.

```php
public $content_model
```





**See Also:**

* \HTMLPurifier_ContentSets - for how this is parsed and then transformed
into an HTMLPurifier_ChildDef.

***

### content_model_type

Value of $child->type, used to determine which ChildDef to use,
used in combination with $content_model.

```php
public $content_model_type
```






***

### descendants_are_inline

Does the element have a content model (#PCDATA | Inline)*? This
is important for chameleon ins and del processing in
HTMLPurifier_ChildDef_Chameleon. Dynamically set: modules don't
have to worry about this one.

```php
public $descendants_are_inline
```






***

### required_attr

List of the names of required attributes this element has.

```php
public $required_attr
```

Dynamically populated by HTMLPurifier_HTMLDefinition::getElement()




***

### excludes

Lookup table of tags excluded from all descendants of this tag.

```php
public $excludes
```






***

### autoclose

This tag is explicitly auto-closed by the following tags.

```php
public $autoclose
```






***

### wrap

If a foreign element is found in this element, test if it is
allowed by this sub-element; if it is, instead of closing the
current element, place it inside this element.

```php
public $wrap
```






***

### formatting

Whether or not this is a formatting element affected by the
"Active Formatting Elements" algorithm.

```php
public $formatting
```






***

## Methods


### create

Low-level factory constructor for creating new standalone element defs

```php
public static create(mixed $content_model, mixed $content_model_type, mixed $attr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content_model` | **mixed** |  |
| `$content_model_type` | **mixed** |  |
| `$attr` | **mixed** |  |





***

### mergeIn

Merges the values of another element definition into this one.

```php
public mergeIn(\HTMLPurifier_ElementDef $def): mixed
```

Values from the new element def take precedence if a value is
not mergeable.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_ElementDef** |  |





***

### _mergeAssocArray

Merges one array into another, removes values which equal false

```php
private _mergeAssocArray(mixed& $a1, mixed $a2): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a1` | **mixed** | Array by reference that is merged into |
| `$a2` | **mixed** | Array that merges into $a1 |





***


***
> Automatically generated on 2025-03-15
