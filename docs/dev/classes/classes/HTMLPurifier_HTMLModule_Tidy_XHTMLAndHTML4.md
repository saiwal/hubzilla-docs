
# HTMLPurifier_HTMLModule_Tidy_XHTMLAndHTML4

Abstract class for a set of proprietary modules that clean up (tidy)
poorly written HTML.



* Full name: `\HTMLPurifier_HTMLModule_Tidy_XHTMLAndHTML4`
* Parent class: [`\HTMLPurifier_HTMLModule_Tidy`](./HTMLPurifier_HTMLModule_Tidy.md)




## Methods


### makeFixes

Defines all fixes the module will perform in a compact
associative array of fix name to fix implementation.

```php
public makeFixes(): array
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

Lazy load constructs the module by determining the necessary
fixes to create and then delegating to the populate() function.

```php
public setup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### getFixesForLevel

Retrieves all fixes per a level, returning fixes for that specific
level as well as all levels below it.

```php
public getFixesForLevel(string $level): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$level` | **string** | level identifier, see $levels for valid values |


**Return Value:**

Lookup up table of fixes




***

### makeFixesForLevel

Dynamically populates the $fixesForLevel member variable using
the fixes array. It may be custom overloaded, used in conjunction
with $defaultLevel, or not used at all.

```php
public makeFixesForLevel(array $fixes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fixes` | **array** |  |





***

### populate

Populates the module with transforms and other special-case code
based on a list of fixes passed to it

```php
public populate(array $fixes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fixes` | **array** | Lookup table of fixes to activate |





***

### getFixType

Parses a fix name and determines what kind of fix it is, as well
as other information defined by the fix

```php
public getFixType(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** | String name of fix |





***

### makeFixes

Defines all fixes the module will perform in a compact
associative array of fix name to fix implementation.

```php
public makeFixes(): array
```












***


***
> Automatically generated on 2025-03-15
