
# HTMLPurifier_HTMLModule

Represents an XHTML 1.1 module, with information on elements, tags
and attributes.



* Full name: `\HTMLPurifier_HTMLModule`



## Properties


### name

Short unique string identifier of the module.

```php
public $name
```






***

### elements

Informally, a list of elements this module changes.

```php
public $elements
```

Not used in any significant way.




***

### info

Associative array of element names to element definitions.

```php
public $info
```

Some definitions may be incomplete, to be merged in later
with the full definition.




***

### content_sets

Associative array of content set names to content set additions.

```php
public $content_sets
```

This is commonly used to, say, add an A element to the Inline
content set. This corresponds to an internal variable $content_sets
and NOT info_content_sets member variable of HTMLDefinition.




***

### attr_collections

Associative array of attribute collection names to attribute
collection additions. More rarely used for adding attributes to
the global collections. Example is the StyleAttribute module adding
the style attribute to the Core. Corresponds to HTMLDefinition's
attr_collections->info, since the object's data is only info,
with extra behavior associated with it.

```php
public $attr_collections
```






***

### info_tag_transform

Associative array of deprecated tag name to HTMLPurifier_TagTransform.

```php
public $info_tag_transform
```






***

### info_attr_transform_pre

List of HTMLPurifier_AttrTransform to be performed before validation.

```php
public $info_attr_transform_pre
```






***

### info_attr_transform_post

List of HTMLPurifier_AttrTransform to be performed after validation.

```php
public $info_attr_transform_post
```






***

### info_injector

List of HTMLPurifier_Injector to be performed during well-formedness fixing.

```php
public $info_injector
```

An injector will only be invoked if all of it's pre-requisites are met;
if an injector fails setup, there will be no error; it will simply be
silently disabled.




***

### defines_child_def

Boolean flag that indicates whether or not getChildDef is implemented.

```php
public $defines_child_def
```

For optimization reasons: may save a call to a function. Be sure
to set it if you do implement getChildDef(), otherwise it will have
no effect!




***

### safe

Boolean flag whether or not this module is safe. If it is not safe, all
of its members are unsafe. Modules are safe by default (this might be
slightly dangerous, but it doesn't make much sense to force HTML Purifier,
which is based off of safe HTML, to explicitly say, "This is safe," even
though there are modules which are "unsafe")

```php
public $safe
```






***

## Methods


### getChildDef

Retrieves a proper HTMLPurifier_ChildDef subclass based on
content_model and content_model_type member variables of
the HTMLPurifier_ElementDef class. There is a similar function
in HTMLPurifier_HTMLDefinition.

```php
public getChildDef(\HTMLPurifier_ElementDef $def): \HTMLPurifier_ChildDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_ElementDef** |  |


**Return Value:**

subclass




***

### addElement

Convenience function that sets up a new element

```php
public addElement(string $element, string|bool $type, string|\HTMLPurifier_ChildDef $contents, array|string $attr_includes = array(), array $attr = array()): \HTMLPurifier_ElementDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **string** | Name of element to add |
| `$type` | **string&#124;bool** | What content set should element be registered to?<br />Set as false to skip this step. |
| `$contents` | **string&#124;\HTMLPurifier_ChildDef** | Allowed children in form of:<br />&quot;$content_model_type: $content_model&quot; |
| `$attr_includes` | **array&#124;string** | What attribute collections to register to<br />element? |
| `$attr` | **array** | What unique attributes does the element define? |


**Return Value:**

Created element definition object, so you
can set advanced parameters




**See Also:**

*  - HTMLPurifier_ElementDef:: for in-depth descriptions of these parameters.

***

### addBlankElement

Convenience function that creates a totally blank, non-standalone
element.

```php
public addBlankElement(string $element): \HTMLPurifier_ElementDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **string** | Name of element to create |


**Return Value:**

Created element




***

### addElementToContentSet

Convenience function that registers an element to a content set

```php
public addElementToContentSet(string $element, string $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **string** | Element to register |
| `$type` | **string** | Name content set (warning: case sensitive, usually upper-case<br />first letter) |





***

### parseContents

Convenience function that transforms single-string contents
into separate content model and content model type

```php
public parseContents(string $contents): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$contents` | **string** | Allowed children in form of:<br />&quot;$content_model_type: $content_model&quot; |





***

### mergeInAttrIncludes

Convenience function that merges a list of attribute includes into
an attribute array.

```php
public mergeInAttrIncludes(array& $attr, array $attr_includes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** | Reference to attr array to modify |
| `$attr_includes` | **array** | Array of includes / string include to merge in |





***

### makeLookup

Convenience function that generates a lookup table with boolean
true as value.

```php
public makeLookup(string $list): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list` | **string** | List of values to turn into a lookup |


**Return Value:**

array equivalent of list




***

### setup

Lazy load construction of the module after determining whether
or not it's needed, and also when a finalized configuration object
is available.

```php
public setup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


***
> Automatically generated on 2025-03-18
