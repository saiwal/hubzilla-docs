
# HTMLPurifier_HTMLModule_NonXMLCommonAttributes

Represents an XHTML 1.1 module, with information on elements, tags
and attributes.



* Full name: `\HTMLPurifier_HTMLModule_NonXMLCommonAttributes`
* Parent class: [`\HTMLPurifier_HTMLModule`](./HTMLPurifier_HTMLModule.md)



## Properties


### name

Short unique string identifier of the module.

```php
public $name
```






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



## Inherited methods


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
> Automatically generated on 2025-03-15
